
> [!TODO] ToDo
> Update for lastest UI Changes, including "Use Breakpoints".

The Full (GCS) character sheet and the Combat sheet both contain four "resource trackers" -- widgets whose job it is to view and manage quantities that increase or decrease with use. This is meant as a generic way to track resources important to the character.

These resources could be physical objects, such as crossbow bolts, bullets, or magic beans, or abstract quantities like control points (from [Fantastic Dungeon Grappling](https://gamingballistic.com/product/fantastic-dungeon-grappling-pdf-dfrpg/)), Quintessence Points ("The Fifth Attribute", [Pyramid 3/120](http://www.warehouse23.com/products/pyramid-number-3-slash-120-alternate-gurps-v)), or Destiny Points ([Monster Hunters](http://www.sjgames.com/gurps/books/monsterhunters/)).

### User Interface
This is what the Resource Trackers look like on the character sheet:

![[Pasted image 20260721131703.png]]

This example shows one 'used' Resource Tracker (Crossbow Bolts) and three trackers currently _unassigned_ to any value. The darker background on the title bar shows that a specific tracker is currently in use.

In the bottom-right corner of each tracker are the configured minimum and maximum values for that tracker. In this case, the minimum for the Crossbow Bolts is zero (0) and the maximum is 20.

You'll also see text like 'Normal' below the input buttons and field. This is intended to reflect the 'status' of the resource, based on the current value and its maximum value. The status may also be colored as another hint of the status of that resource. For example:

![[Pasted image 20260721131727.png]]
### Editing the current value
_Increment/Decrement Buttons_: You can increment or decrement the count of a tracker by clicking on the [+] or [–] buttons. Each click increases or decreases the current count by 1. Holding the Shift key down and clicking will increase or decrease the count by 5.

_Reset Button_: Clicking the curved arrow button [⟲] resets the tracker to its maximum value (unless the Resource Tracker is a “Damage Tracker”, in which case it resets it to 0).

_Resource Value Textfield_: If you click into the text area, you can directly edit the value as well.

![[Pasted image 20260721131904.png]]

_Quick Access Ribbon_: If you click into the text area, a popup 'ribbon' will appear with buttons to increase or decrease the current value by 1, 5, or 10, set it to zero (0), or reset it to the current value (useful if you've clicked a number of those buttons but want to cancel the action).

### Customizing the Resource Tracker
The simplest use of the Resource Tracker requires very little setup. It involves naming the resource and optionally setting its maximum value, and some 'thresholds' that serve as rules the tracker uses to display the Status Text and its color.

To edit a tracker, click on its titlebar (it shows a pencil icon) which opens a dialog that asks you what you want to do:

![[Pasted image 20260721131928.png]]

_Edit Tracker_: This will open the Tracker Editor, allowing you to change the configuration of this tracker.

_Delete Tracker_: This clears all configuration in the Resource Tracker, making it unassigned.

_Copy Template_: This allows you to copy the Resource Tracker configuration from a template defined for this game world. This makes it easy for the GM to define a standard resource that many or all characters should have. Clicking this button will copy the template named in the "Resource Tracker Templates" dropdown list into this specific Resource Tracker. This _overwrites_ any current configuration of the selected Resource Tracker.

#### Edit Tracker
Clicking the Edit Tracker button opens the Resource Tracker Editor in its own window.

![[Pasted image 20260721131955.png]]

_Resource Name_: The only required configuration in a tracker is its name. This changes the name of the Resource Tracker on the character sheet and sets the titlebar color to black, showing that this Resource Tracker "slot" is in use.

_Current_: A number to use as the initial tracker value.

_Minimum_: The minimum value of the resource. At the moment this is informational only; it doesn't affect the tracker in any way. E.g., it does not prevent the resource from going below this value.

_Maximum_: The maximum value of the resource. It is potentially used in determining the Status Text and color. However, the resource value is not restricted from exceeding this value.

_Alias_: A short name used to refer to this resource. It is required if you want the resource to show up in the Apply Damage Dialog as a target of damage.

_Reference_: A GURPS PDF page reference, used by PDFoundry to open the appropriate PDF inside Foundry. If entered, the bottom-left corner of the tracker will contain a link to open the PDF to the indicated page.

_Use as Damage Type_: If checked, this allows the resource to be used in the Apply Damage Dialog as a target of damage (see [[Apply Damage Dialog!]]).

_Damage Tracker_: The assumption is that most resources start at a maximum value, and "damage" is represented by _subtracting_ from the resource. This is the default behavior and reflects how HP and FP work. If this checkbox is checked, then "damage" is _added_ to the current value (instead of subtracted). The damage is “tracked”. This is how the “Control Points” Resource Tracker works (from [Fantastic Dungeon Grappling](https://gamingballistic.com/product/fantastic-dungeon-grappling-pdf-dfrpg/)).
#### Thresholds
Thresholds are used to set up ranges of values that correlate to a specific status of the resource. This is how you can customize the Status Text and its color in the tracker, and have it update automatically as the resource value increases and decreases.

You need to create one threshold for each status you want to display. The current resource status is determined by comparing the current value to its maximum value.

Clicking the '+' button will create a new threshold.

![[Pasted image 20260721132120.png]]

For each threshold, you need to define the following information:

_Comparison_: This is the type of comparison to do between the current value and threshold value (which is defined by the next two fields, _Operator_ and _Value_). Possible values are:

- > Greater Than
- ≥ Greater Than or Equal To
- < Less Than
- ≤ Less Than or Equal To

_Operator_: A mathematical operator to apply to the resource's maximum value to get the threshold value. Possible values:

- [MAX ×] - The resource maximum value _times_ (or multiplied by) the next value
- [MAX ÷] - The resource maximum value _divided by_ the next value
- [MAX +] - The resource maximum value _plus_ the next value
- [MAX –] - The resource maximum value _minus_ the next value

_Value_: The value to use in the calculation of the threshold value.

_Condition_: The name of the status.

_Color_: The color you want to assign to the status.

The trashcan icon is used to delete this threshold.
#### Important Concepts
_Threshold Value_: The threshold value is calculated by applying the _Operator_ to the resource maximum and the _Value_.

For example, suppose we have a Resource whose maximum value is 15. If the _Operator_ is [MAX +] and the _Value_ is 5, then the _Threshold Value_ is (15 + 5), or 20.

_Resource Status_: To determine the current status of a resource, **the current value is compared, one-by-one, to each _Threshold Value_ starting from the top of the list and moving towards the bottom**. The first calculation that is 'true' is used as the _Resource Status_.

For example, assume we have the following list of thresholds:

![[Pasted image 20260721132255.png]]

Also assume that the resource maximum is 18.

If the value of the the Resource Tracker is:

- 20
    - Is 20 greater than 18 (MAX × 1)? _Yes. The status is **Over**._
- 18
    - Is 18 greater than 18 (MAX × 1)? _No._
    - Is 18 greater than 9 (MAX ÷ 2)? _Yes. The status is **Normal**._
- 3
    - Is 3 greater than 18 (MAX × 1)? _No._
    - Is 3 greater than 9 (MAX ÷ 2)? _No._
    - Is 3 greater than 0 (MAX × 0)? _Yes. The status is **Low**._
- 0
    - Is 0 greater than 18 (MAX × 1)? _No._
    - Is 0 greater than 9 (MAX ÷ 2)? _No._
    - Is 0 greater than 0 (MAX × 0)? _No._
    - Is 0 less than or equal to 0 (MAX × 0)? _Yes. The status is **Under**._

Here's another example that copies the logic used to track Fatigue. I hope this makes it easier to understand how to set thresholds to drive the correct Status Text and color.

For FP, the possible statuses are (see page B426):

**Normal**: The current FP value is _greater than or equal to_ 1/3 your basic (Max) FP.

**Very Tired**: The current FP value is _less than_ 1/3 of your basic (Max) FP but _greater than_ zero (0).

**Verge of Collapse**: The current FP is _less than or equal to_ zero (0) and _greater than_ -1 × basic (Max) FP.

**Unconscious**: The current FP is _less than or equal to_ -1 × basic (Max) FP.

You could make a Resource Tracker that works like Fatigue, you would create thresholds like this:

![[Pasted image 20260721132343.png]]

---
### Typical Uses
The following are some examples that you can copy to get some basic Resource Tracker functionality.
#### Ammunition
Use a resource tracker to track the bullets in a clip or magazine. In this example, the magazine contains 22 bullets. You want to show the Status Text as "OK" with a green highlight while there are more than 6 bullets in the magazine; as "Running Low" with a yellow highlight if there are 1-6 bullets, and "Empty" with red highlight if the magazine is empty.

![[Pasted image 20260721132410.png]]
#### Shield Damage
Use a resource tracker to track the HP of a shield and have the ability to apply normal damage to the shield instead of the character. Let's assume we are talking about a _Large Shield_ (B287) with DR 9, HP 60.

![[Pasted image 20260721132456.png]]

**Normal**: Shields provide their normal protection as long as their current HPs are greater than zero (0).

**Disabled**: If equal to or less than zero (0), but greater than -5×HP, the shield must make a HT roll or is disabled or destroyed, and no longer provides any protection. It is still attached to the wearer and encumbers them.

**Collapse**: At equal to or less than -5×HP but greater than -10×HP, the shield automatically fails but is still attached/worn.

**Destroyed**: At less than or equal to -10×HP the shield is totally physically destroyed and falls off the wearer.

NOTE: To be able to apply damage directly to this tracker, it requires the alias to be defined (in this case “shield”) and the "Use as Damage Type" box must be checked.

![[Pasted image 20260721132524.png]]

With this setup, you can drag a damage chat onto this character, and when the ADD pops up, select Apply To: "Large Shield". You'd have to override the DR to be the DR of the shield, and select the Injury Tolerance: Homogenous, then Apply Injury to damage the shield.

![[Pasted image 20260721132541.png]]

![[Pasted image 20260721132548.png]]
