## How to play
Once all of your characters are imported into the system, you can play. We have a [Players Guide](https://youtu.be/x-xD39x_JQw) video to help you get you started.

# Dice Roller
Near the bottom of the screen there is an image of 3d6.
![[Pasted image 20260720165831.png]]

Use this to make a 3d6 roll by clicking on it, or a 1d roll by right-clicking. If there are any [[#Modifiers]] in the Modifier Bucket, the die roll will be adjusted by the modifier total.
## Character Sheet
There are multiple character sheets available, including some from external modules, but the ones that come with GGA fall into two general categories:

- Full (GCS) sheet
- Modern sheet

Although there are several other sheets, most are based on one of these two.
## Full (GCS) Sheet
This sheet is interactive; clicking on attributes, skill levels, dodge scores, modifiers, etc., will make an in-game action.

![[Pasted image 20260720163413.png]]
## Rollable Fields
Notice that the mouse is hovering over this character's IQ attribute and it is highlighted in a gold-orange color. This indicates that this attribute is rollable; clicking it will automatically make a GURPS success roll against this character's IQ and display the results in the chat bar (perhaps with a [[Miscellaneous Settings#Show Confirmation Roll Dialog|Roll Confirmation]]  dialog).

In general, rollable fields (such as attributes) are highlighted in yellow.

![[Pasted image 20260720163727.png]]

If you get the Roll Confirmation dialog, click **Roll** to complete the roll or **Cancel**.

![[Pasted image 20260720163949.png]]
_Figure: The results of the roll is shown in the chat. Notice that the character's name, the type of roll (**vs IQ**), target (**10**),  individual dice (**2, 1, 1**), result (**Critical Success**) and margin of success (**6**) are all displayed._

Skills and Spells are all augmented with rollable fields.
![[Pasted image 20260720173832.png]]
## Modifiers
Modifiers are highlighted in orange (see the Penalty column of the Hit Location table), green (positive modifiers like the Margin of Success button on the chat message), or red (other negative modifiers).

To see how to modify a roll, let's look at the Tabbed Sheet (based on the Full (GCS) Sheet).
![[Pasted image 20260720165301.png]]

If Björn wants to shoot his Composite Bow using one of his Bodkin arrows at a foe 8 yards away, targeting the Vitals, the player would need to apply penalties for range and Hit Location.

Notice the Size and Speed/Range and the Hit Location tables are on the character sheet. To add those penalties to Björn's shot, the player would click on the –4 modifier on the Speed/Range table for range 8 and the –3 penalty for Vitals (see the Penalty column). Björn has the Heroic Archer advantage, so he also gets the bonus for Accuracy (Acc) without aiming. Click the modifier in the Acc column of the Weapon table for this weapon (Composite Bow (Bodkin), +4).

After clicking those penalties, you should see a total modifier of –3 in the [[Modifier Bucket TODO]] window near the bottom of the screen:
![[Pasted image 20260720170530.png]]

The Modifier Bucket keeps track of all modifiers applied before a roll is made. This section of the User Guide will not go into details about all the features of the Modifier Bucket; refer to that section of the User Guide for more information.

If you mess up the modifiers, or need to change one or more of them, clicking on the trashcan icon in the Modifier Bucket widget removes all modifiers.

Okay, you have the modifiers for this attack roll set. To make the attack, click either the **Level** or **Usage** field of the Weapon you want to use.
![[Pasted image 20260720170618.png]]

Note that the Roll Confirmation window shows Björn's adjusted skill level: 16 (19 – 3 for modifiers).

Here's the roll results chat message:
![[Pasted image 20260720170800.png]]
_Figure: It's nice to have a high skill!_

Note that the results chat message also lists the modifiers applied.
### A Special Note About Modifiers
While using modifiers in this way is simple, it has some disadvantages. Basic modifiers like this do not know what they are modifying. If you put both modifiers to skill to hit with a melee weapon and a modifier to damage into the Modifier Bucket at the same time, all of these modifiers are used on the next dice roll. [[Tagged Modifiers]] are the solution to this!
## Hit Points and Fatigue
These resources have dedicated UI controls:
![[Pasted image 20260720172253.png]]

The **Basic** value is the resource maximum. 

The value in the textfield is the current value. You can click into the textfield and enter a new value for the resource.

The colored line below the textfield displays the current status of the character based on depletion of the resource (HP ranges from Healthy, Reeling, Collapse, Check #1, ..., Check #4, Dead, Destroyed).

The [+] button adds 1 to the resource; [–] subtracts one. The [⟲] button resets the resource to its maximum.

You can enable a quick edit ribbon on these components via the [[Actor Settings#Enhanced Numeric Inputs]] setting.
## Encumbrance, Move & Dodge
This widget is used to display the character's current Encumbrance level based on the weight they are carrying, and the associated Move and Dodge values.
![[Pasted image 20260720173209.png]]
The current encumbrance level is highlighted in yellow and has an arrow indicating it.

If the character has more than one move mode — e.g., they have the Flight advantage — the Mode dropdown can be used to select their current movement mode, and that will update the current Move value.

Clicking the Dodge value in the current encumbrance level will make a Dodge roll and post the results in chat.
## Self-Control Rolls
Some disadvantages have self-control (CR) values. When GGA imports the character, it turns the CR value into a rollable field.

![[Pasted image 20260720173636.png]]

Clicking on the highlighted text will make the CR roll and post the results in chat.

## Other UI Elements
Other UI elements are documented in dedicated sections of the User Guide:
- [[Modifier Bucket TODO]]
- [[Resource Tracker]]
- [[Combat Tracker TODO]]
- [[Apply Damage Dialog]]
- [[Effect Modifiers TODO]] and [[Tagged Modifiers]]
- [[Rollable Tables TODO]]