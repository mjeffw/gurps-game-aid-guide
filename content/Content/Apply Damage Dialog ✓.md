Settings: [[Damage Settings]]

Damage calculation in GURPS can get rather complex. To get started, you might watch this video: [how to apply damage](https://www.youtube.com/watch?v=6eaCyacs4N0).

> [!TODO] ToDo
> Update for latest changes, including multiple hits and applying effects.

## Applying Damage to a Token or Character
Once you've rolled for damage, there will be a Damage Chat message in the log, similar to this:

![[Pasted image 20260721162323.png]]

It shows the damage die roll and the result of rolling the dice and adding modifiers. If you've targeted a specific foe, it will also have the **Apply All to \<enemy-name\>** button. If that was the correct target, you can simply click the button to start the Apply Damage process.

Whether or not the **Apply All to \<enemy-name\>** button is present, you can also click on the section of the message in the box (with "7 points of damage") and drag it. It will turn into a blood splatter icon. Drop it on either a token on the canvas, on an open character sheet, or on a combatant listed in the [[Combat Tracker]].

Once applied to a target, the Apply Damage Dialog pops up.

![[Pasted image 20260721165034.png]]
## Apply Damage Dialog
The ADD will have certain information already selected:

- The Attacker's token artwork. 
- The **Target**'s name and artwork (Stóralf Elder)
- The **Amount of Damage** to apply (28)
- Which **Resource** to subtract from (HP)
- The **Hit Location** (Torso). This is determined by the [[Damage Settings#Default Hit Location]] setting. If set to **Random** , you'll see another die roll occur as GGA determines the specific hit location based on that roll.
- The **DR** (3) of the Hit Location.
- **Large-Area Injury**. 
- The **Damage Type** (cr); taken from the damage roll, and the appropriate **Wounding Modifier** for that damage type and hit location. (This assumes setting [[Damage Settings#Location Wounding Modifiers]] is checked ✅.)
- Any of the myriad special modifiers and other effects from the GURPS rules that GGA supports and can detect. (Effects marked with † are detected and applied automatically.) 
	- Half-Damage (**1/2D**) for Ranged attacks.
	- **Vulnerabilities**.
	- **Armor Divisor**†, from the damage die roll.
	- **Hardened DR** level.
	- **Injury Tolerance**†
	- **Damage Reduction**†
	- **Explosion**
	- **Flexible Armor** for calculating **Blunt Trauma**.
	- **Shotgun at Extremely Close Range**.

Other effects and more automatic detection of them are planned for the future.

In the **Calculation & Results** area of the ADD are:

- The math that determines the final injury. 
- A list of effects that maybe applied based on the damage (**Shock**, in this case). Includes Blunt Trauma (assumes setting [[Damage Settings#Blunt Trauma]] is checked ✅), Shock, Knockback, Major Injury, Head or Vitals Hit, and Crippling (Limbs).
- The final damage to apply and an option to apply it multiple times.
### Overrides
All of this information can be overridden as necessary.
#### Amount of Damage to Apply
Typing a new value into the **Directly Apply** textfield overrides the initial value that will be put through the damage calculator to get final damage.
#### Resource 
Select a new value from the dropdown (next to the Directly Apply textfield) to change which resource the injury will be applied to.
#### Hit Location and DR
- Directly click on a Hit Location radio button to change the selection; the ADD will update all other fields to match.
- Click the **Random** button to randomly select another location.
- Select **Large-Area Injury**. Selecting this will override the DR to the average of all DR across the character's Hit Locations.
- Override the DR by entering a value in the **Override DR for Location** textfield.
#### Type & Wounding Modifiers
- Select **No Modifier** to remove all wounding modifiers.
- Select and enter a value into the **Enter Modifier** textfield to override it.
- Any additional modifier value may be entered in **Additional Modifier**. This value will be added to the modifier otherwise selected. For example, Large Piecing (pi+) against the Torso gives a 1.5 modifier; If the value "1" is entered into Additional Modifier, the total wounding modifier becomes 2.5 (1.5 + 1).
#### Special Situations
Select any of these (and in some cases provide a value) to turn on or off that effect from the damage calculation.
#### Total Injury and Mutiple Times
In the bottom right of the ADD, you can override the total points of Injury to apply — effectively ignoring the ADD's calculations. You can also change how many times to apply this damage.

## Damage Results
The ADD tries to calculate possible side-effects of taking damage such as Knockback, Major Wounds, Crippling, etc. Those effects are listed in the bottom center of the ADD.

![[Pasted image 20260721172124.png]]

None of these are automatically applied.

Next to each is a series of buttons:
- ![[Pasted image 20260721172535.png]] - Adds the effect to the target
- ![[Pasted image 20260721172603.png]] - Adds a chat command that, if executed, applies the effect to any selected token. If there is a roll to reduce or avoid the effect, that check will be part of the chat command.
- ![[Pasted image 20260721172724.png]] - If there is a roll to avoid or reduce the effect, do the (blind) roll for the target and apply if the roll fails.

![[Pasted image 20260721173114.png]]
_Figure: Applying Knockback to a character via the chat command. The GM will have to move the Stóralf Elder two hexes manually. Clicking on the "Roll DX-1, Acrobatics-1, or Judo-1 or fall!" button will make that roll automatically and if it FAILS, will change the posture of the target to Prone. The "+4 for Perfect Balance" button may be clicked before the DX/Acrobatic/Judo check to add a +4 bonus to that roll._

![[Pasted image 20260721173807.png]]
_Figure: The GM clicked the "Dice" button next to a Major Wound, and GGA rolled the HT check for the Stóralf and added the Stunned and Prone effects to it since the roll failed._

> [!NOTE]
> Applying the damage before resolving these effects closes the ADD, and then you don't have those buttons anymore! A solution is simply to reapply the damage to the target, resolved the effects from the new instance of the ADD, and then close the ADD without applying the Injury by clicking on the window **ＸClose** button.

## Applying Injury
The Apply Injury button is also a dropdown allowing you to change _how_ you want the window to behave:
- **Apply Injury** - Apply the injury publicly and close the ADD. Others can see the injury and potentially the Show the Math data in the chat.
- Apply Injury (Qu**ietly)** - Only the GM and the Player owner of the target can see the Injury information. The ADD closes.
- **Apply Injury/Keep Open** - As **Apply Injury**, but don't close the ADD.
- **Apply Injury (Quietly)/Keep Open** - As **Apply Injury (Quietly)**, but don't close the ADD.

With setting [[Damage Settings#Default Action for ADD]] set to **'Target'**, the ADD will **Apply Injury** to Player Characters and **Apply Injury (Quietly)** to NPCs and Monsters.
