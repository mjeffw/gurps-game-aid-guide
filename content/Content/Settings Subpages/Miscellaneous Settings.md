## Mook Generator Defaults
Allows you to change the default values of Attributes, Melee and Ranged Attacks, Traits, Skills, Spells, Equipment, and Notes used to create Quick-and-Dirty mooks using the [[Mook Generator]].
## Use Quick Roll Button
Allows the user to turn off or on a "Quick Roll" button displayed for each combatant in the [[Combat Tracker TODO]], and which rolls to include in the resulting popup panel. Rolls may include Attributes, Secondary Checks, Attack Rolls, Defense Rolls, or selected Skills and Spells from the character sheet.
## Use Tagged Modifiers
Use this option to turn off/on and configure tagged modifiers. A [[Tagged Modifiers]] is a way to categorize bonuses by type of roll so that, for example, a bonus to damage will only apply to damage rolls.
> [!NOTE] Recommended Value
> Keep defaults settings.
## PDF Settings
Allows you to configure a couple of [[PDF Link]] behaviors:
- **Basic Set PDF**: Use this setting to configure whether you own the combined Basic PDF (Characters and Campaigns in a single PDF) or if you have separate PDFs (GURPS Characters in one PDF file, GURPS Campaigns in another PDF file). This will allow the system to open the correct PDF file even when the PDF link doesn't distinguish between the two. For example, setting this to **Separate (Characters, 'B'; Campaigns, 'BX')** "_B101_" will open the GURPS Character pdf to page 101 -- the Trait Modifiers chapter -- while "_B400_" will open GURPS Campaigns to page 400 (Grappling and Hit Location rules).
- **Open first PDF found**: If checked, only the first PDF that is both listed and present in your collection will be opened when a PDF link is clicked. Otherwise, all PDF books found will be opened.
## Show Read Me on Version Change
If checked, the Read Me document will be displayed the first time you join the campaign world after a GGA software update.
## Use Physical Dice
If checked, TRUSTED players will be prompted for all dice rolls. For example, if a Trusted player clicks on his IQ attribute to roll against it, the system will pop up a dialog asking him to enter either the total of the 3d roll, or the individual die rolls. For example, the player could enter either "13" or "6, 2, 5" and that value will be accepted as the roll. 

This is a great way to use Foundry for in-person gaming where the players want to roll their own dice.
![[90086520-F892-487C-B671-C690515EB1F8_1_105_c.jpeg]]
## Player Chat Commands are Private
If checked, most player chat commands will be visible only to that player, instead of to everyone. Use this if you trust your players and don't want to see the chat fill up with their chat commands.

![[Pasted image 20260719155659.png]]
_Figure: A player-entered chat command to add +1 FP — visible because this setting is set to unchecked. If checked, there is no chat message visible to other players or GM._
## Portrait Path
Choose whether imported character portraits are stored **globally** (and thus available in any world) or **locally** (available only in the current world.).
## Show Confirmation Roll Dialog
If checked, a confirmation dialog will display after making a roll. The roll is not made until the player confirms it via this dialog.
> [!NOTE] Recommended Value
> Checked

![[Pasted image 20260719160619.png]]
_Figure: Roll Confirmation Dialog._
## Use Modify Dice + Adds Rule
If checked, use the _Optional Rule: Modify Dice + Adds_ rule in Basic Characters, p. 269, to modify damage rolls by converting large adds as additional dice. For instance, `2d+5` becomes `3d+1` using this rule.

![[Pasted image 20260719161156.png]]
_Figure: In the screenshot above, the player clicked on his Broadsword damage (2d+2 cut) after adding another +7 damage to the modifier bucket. The result is 4d+2 using this rule._
## Show Effect Modifier Popup
If checked the [[Effect Modifiers TODO]] popup window will be displayed by default.
![[Pasted image 20260719162238.png]]
_Figure: Effect Modifiers popup displaying for Björn, who is currently kneeling and Aimed on this last turn._
## Quick Sheet
This setting determines which other Character Sheet is displayed if you click on the [⇆] button in the title bar of the character sheet. Clicking this button toggles back and forth between the default sheet and the value of this Quick Sheet setting.