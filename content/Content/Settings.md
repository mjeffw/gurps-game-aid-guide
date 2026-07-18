## Mook Generator Defaults
Allows you to change the default values of Attributes, Melee and Ranged Attacks, Traits, Skills, Spells, Equipment, and Notes used to create Quick-and-Dirty mooks using the [[Mook Generator]].
## Show Item Image in Character Sheet
Allows you to turn on or off an image associated with Traits, Skills, Spells, or Equipment on the character sheet. 

A cool way to show the image of a magic item directly on the sheet, for example.
## Bucket Journal Entries
Use this to select Journal Entries to show as a panel in the [[Modifier Bucket]] for a collection of custom modifiers.
## Use Quick Roll Button
Allows the user to turn off or on a "Quick Roll" button displayed for each combatant in the [[Combat Tracker]], and which rolls to include in the resulting popup panel. Rolls may include Attributes, Secondary Checks, Attack Rolls, Defense Rolls, or selected Skills and Spells from the character sheet.
## Use Tagged Modifiers
Use this option to turn off/on and configure tagged modifiers. A [[Tagged Modifier]] is a way to categorize bonuses by type of roll so that, for example, a bonus to damage will only apply to damage rolls.
## Color Character Sheet
Allows you to selectively override the colors of the Full (GCS) Character Sheet.
## PDF Settings
Allows you to configure a couple of [[PDF Link]] behaviors:
- **Basic Set PDF**: Use this setting to configure whether you own the combined Basic PDF (Characters and Campaigns in a single PDF) or if you have separate PDFs (GURPS Characters in one PDF file, GURPS Campaigns in another PDF file). This will allow the system to open the correct PDF file even when the PDF link doesn't distinguish between the two. For example, setting this to **Separate (Characters, 'B'; Campaigns, 'BX')** "_B101_" will open the GURPS Character pdf to page 101 -- the Trait Modifiers chapter -- while "_B400_" will open GURPS Campaigns to page 400 (Grappling and Hit Location rules).
- **Open first PDF found**: If checked, only the first PDF that is both listed and present in your collection will be opened when a PDF link is clicked. Otherwise, all PDF books found will be opened.
## Resource Tracker Manager
Allows you to create and apply standard [[Resource Tracker]] instances to character sheets. Resource trackers provide the user with a way to track non-standard values and pools such as Energy Reserve for the GURPS magic system or shield damage, etc.

## Show Document Debug Info
When checked, each character sheet will display a Debug icon in the title bar. Clicking this will so the data model of that actor. This is primarily of interest to users who want to write macros to automate some piece of functionality.
## Show Read Me on Version Change
If checked, the Read Me document will be displayed the first time you join the campaign world after a GGA software update.
## UI: Show 3D6 (Next to Modifier Bucket)
If checked the system will display the dice roller shortcut next to the Modifier Bucket. Clicking this will roll 3D6; Ctrl- or Option-click will roll 1D6.
## Use Physical Dice
If checked, TRUSTED players will be prompted for all dice rolls. For example, if a Trusted player clicks on his IQ attribute to roll against it, the system will pop up a dialog asking him to enter either the total of the 3d roll, or the individual die rolls. For example, the player could enter either "13" or "6, 2, 5" and that value will be accepted as the roll. 

This is a great way to use Foundry for in-person gaming where the players want to roll their own dice.
## Use Quintessence
If checked, this adds the Quintessence attribute and adds a Quintessence Points Resource Tracker to all characters. 

_This functionality will eventually be replaced by implementing custom attributes in GGA v1.0+._
## Import Settings:
The following controls how GGA [[Import from GCA or GCS]] works.
### Ignore 'name' Attribute
If checked, GGA will not update the character's name during import from GCA/GCS if it doesn't match the name in GGA.
### Only TRUSTED Players May Import
If checked, the "Import" button will only be displayed on the character sheet if the player permission level is "Trusted", "Assistant GM", or "Game Master". Use this if you want to tightly control who can update the character.
### Auto Save Foundry Quantity and Count
If checked, this will prevent an Import from GCA/GCS from overwriting the values in the GGA character sheet. This will be useful if you are tracking equipment quantity in GGA.
> [!NOTE] Recommended
> Checked


### Current HP and FP
This setting will control how HP and FP values are saved or set during an import:
- **Ask before overwriting**: Prompt the user to whether the value should be updated or not.
- **Use the Import file value**:  Automatically overwrite the value on the GGA character sheet with the value from GCA/GCS.
- **Ignore the Import file value**: Never update the GGA character sheet's HP and FP from the GCA/GCS values.
### Body Plan/Hit Locations
This setting will control how the Body Plan (Body Type) values are saved or set during an import:
- **Ask before overwriting**: Prompt the user to whether the value should be updated or not.
- **Use the Import file value**:  Automatically overwrite the value on the GGA character sheet with the value from GCA/GCS.
- **Ignore the Import file value**: Never update the GGA character sheet's Body Plan from the GCA/GCS values.
### Import Extended Values from GCS Compendiums
When [[Import GCS Equipment]] compendium, the extended values for weight and cost will be imported. Check this if you don't want or need GGA to calculate the extended value.
### Import File Encoding
What character set to use when importing. Change this if GGA doesn't display Unicode or other characters correctly.
### Use Non-locally Hosted Import Dialog
_This setting is horribly misnamed._ 

If checked, GGA will try to remember the location of the import file after the first import in a session. If successful, the next time you click the import button, it will automatically import the file from that location without prompting you for its location again.
### Use Foundry Items for Player Data
If checked, GGA uses Foundry Items for Traits, Skills, Spells, Equipment, and Melee and Ranged attacks. 
> [!NOTE] Recommended
> Checked

_This functionality will be replaced in GGA v1.0, where Foundry Items is the only data model._
### Overwrite Portraits
If checked, the portrait image on the character sheet will be overwritten by the image used in GCA/GCS during import.
## Actor Settings
### Show Navigation
If checked, show a navigation ribbon at the bottom of the Full (GCS) character sheet. Clicking on a Heading title in the navigation ribbon will automatically scroll the character sheet to show the section with that heading.

![[Pasted image 20260717175309.png]]
*Figure: Navigation Ribbon, shown.*

The navigation ribbon can be hidden or shown by clicking on the double arrows icon (»):
![[Pasted image 20260717175616.png]]
_Figure: Navigation Ribbon, hidden._
### Portrait HP Tinting
If checked, the Modern character sheet will show a red tint overlay to indicate relative HP loss for the character.
![[Pasted image 20260717175946.png]]
_Figure: Character with no HP loss._

![[Pasted image 20260717180042.png]]
_Figure: Character with about 75% HP loss._

![[Pasted image 20260717180141.png]]
_Figure: Character at first death check._
### Enhanced Numeric Inputs
If checked, the Full (GCS) sheet HP and FP trackers will display a popup ribbon with "quick modifier" buttons between –10 and +10. Use this to quickly add or subtract values from the value in addition to directly typing in the new total or using the [+], [–], or [⟲] buttons.
> [!NOTE] Recommended
> Checked
#### Using the Enhanced Numeric Input Ribbon
Click into the text field with the current HP value to display the ribbon. Then use the ribbon buttons to quickly add or subtract values. For example, if this character loses 28 HP, you could do that by clicking –10 twice, –5 once, and –1 three times. 

The ribbon always remembers the original value of the attribute (15, in the image below). If you lose track of how much you've added or removed from the value, you can reset it to the original value by clicking that value (shown in red) on the ribbon.

Clicking the +0 button zeroes out the attribute (sets its value to zero).
![[Pasted image 20260717180832.png]]
_Figure: The Enhanced Numeric Input ribbon._
### Calculate Encumbrance
If checked, GGA will track the weight of all Carried Equipment, and set the appropriate Encumbrance level based on that weight.
> [!NOTE] Recommended
> Checked
### Weight Based on 'Equipped'
If checked, only Carried Equipment with the "Equipped" flag set to true will be included in any weight calculations. This allows a player to unselect "Equipped" to indicate that they have dropped the item.

(Alternatively, the player can move the dropped items to the Other Equipment list.)

![[Pasted image 20260718141307.png]]
_Figure: "Backpack, Small" (and all the items inside it) is unequipped and will not be added to the current weight and encumbrance._
### Remove Unequipped Weapons from Melee and Range Lists
If checked, only equipped Equipment with attacks will be listed in the Melee and Ranged Attack lists.
> [!NOTE] Recommended
> Checked

![[Pasted image 20260718141119.png]]
_Figure: Any attacks from "Broadsword" will not be listed since it is unequipped._
### Display User-Created Flag
If checked, Equipment not imported from GCS/GCA will show a small flag.

![[Pasted image 20260718140747.png]]
_Figure: The blue ribbon icon indicates that "Equipment..." was not imported._
### Display Foundry Item Flag
If checked, show an icon next to an item (Trait, Skill, Spell, Equipment) that is a proper Foundry Item (see [[#Use Foundry Items for Player Data]]).

![[Pasted image 20260718140747.png]]
_Figure: The star icon indicates that "Equipment..." is a Foundry Item._
### Display Foundry Global Item Flag
If checked, a small icon will appear next to any equipment that was dropped from a Foundry Compendium.

![[Pasted image 20260718142301.png]]
_Figure: "Anti-Garrote Collar" was dragged from a GCS Equipment library that was imported into Foundry as a Compendium, as indicated by the book icon._
### Display Quantity/Count Saved Flag
If checked, a small icon will appear after equipment where the Quantity and/or Count will be saved during imports. (See [[#Auto Save Foundry Quantity and Count]]).

![[Pasted image 20260718142900.png]]
_Figure: The "#" icon next to "Bodkin Point Arrow" indicates that the current quantity (11) will be saved during an import._
### Convert 'x2/x5' Range to Yards
If checked, Ranged weapons with ST-derived ranges (such as x2/x5) will be converted in yards for display.
> [!NOTE] Recommended
> Checked

![[Pasted image 20260718143408.png]]
_Figure: Boomerang equipment has a Ranged Attack with a range of "x6/x10"._

![[Pasted image 20260718143609.png]]
_Figure: After adding Boomerang with this setting checked, the calculated range will be displayed (ST 13 means 6x13 = 78 and 10x13 = 130)._
## Modifier Bucket Settings
These settings handle how the [[Modifier Bucket]] is displayed and how it works.
### Show On Mouse Over
If checked, the Modifier Bucket window will appear when the mouse hovers over the icon, like a tooltip. The window is closed automatically if the mouse moves off the window. If unchecked, the window opens if the icon is clicked and closes if the [X Close] button on the title bar is clicked.
### Add Range Ruler Modifier
If checked, the last measurement made by the range ruler will be automatically converted to a modifier based on the Size/Speed and Range table and added to the Modifier Bucket.
> [!NOTE] Recommended
> Checked

![[Pasted image 20260718145054.png]]
_Figure: Range Ruler making a measurement._

![[Pasted image 20260718145235.png]]
_Figure: The resulting range modifier added to the Modifier Bucket._
### Scale Factor
Change the size of the Modifier Bucket; great for adapting for very large or small screens or vision impairment. Ranges from 80% — 120%.
### Change Position
Select the location of the Modifier Bucket: to the left or right of the macro bar.
### Change 3d6 Image
Allows the user to upload an image to use instead of the red 3d6 for the die roller.
## Combat Settings
These settings modify how [[Combat]] works and what options are available.
### Range Modifier Strategy
Allows the user to select how range penalties are calculated:
- **Size and Speed/Range Table**: the standard range calculation.
- **Monster Hunters 2 Range Bands**: The simplified ranges from GURPS Monster Hunters.
- **-1 for every 10 hexes**: A community contributed range calculation.
### Use Size Modifier Difference in Melee
In GURPS Rules-As-Written (RAW) Size Modifier is an absolute modifier — e.g., to target a creature with SM +3 gives a +3 modifier, while a creature with SM -4 is always at -4 modifier to skill. 

Checking this enables an alternative strategy: The difference between target and attacker SM is used instead. So if an SM +3 attacker tries to target a SM -4 creature, the attacker will be a -7 to skill.
### Turn Sequence Formula
Allows the user to modify the standard Turn Sequence calculation. By default, it is `((@basicspeed.value * 100) + (@attributes.DX.value / 100) + (1d6 / 1000)) / 100`, which yields a value like 6.00134 (6 for the character's Basic Move score + 0.0013 for their DX + 0.00004 for a 1d6 roll). This results in the GURPS RAW determination of Turn Sequence order.
> [!NOTE] Recommended
> `((@basicspeed.value * 100) + (@attributes.DX.value / 100) + (1d6 / 1000)) / 100`

Don't change this unless you understand the Foundry actor data model.
### Use On Target Ranged Modifiers
If checked, the additional aiming-related maneuvers and modifiers will be enabled.
### Maneuver Icon Visibility
> [!NOTE] Recommended
> Everyone
### Maneuver Visibility Details
> [!NOTE] Recommended
> General
### Maneuver Updates Move
> [!NOTE] Recommended
> Checked

### Allow Roll Based on Maneuver
> [!NOTE] Recommended
> Warn

### Check for Targets Before Roll
> [!NOTE] Recommended
> Warn

### Allow Roll Before Combat Starts
> [!NOTE] Recommended
> Warn

### Use Max Actions Check
> [!NOTE] Recommended
> All Tokens in Combat
### Automatically Add Cumulative Parry Penalties
> [!NOTE] Recommended
> Checked

### When to add Shock Effect
> [!NOTE] Recommended
> Immediately
## Damage Settings
These settings control how the [[Apply Damage Dialog]] works.
### Restrict ADD to GM

### Simple ADD

### Default Hit Location

### Armor Divisors

### Blunt Trauma

### Location Wounding Modifiers

### Show the Math

### Conditional Injury

### Body Hits

### Default Action for ADD

## Status Effects

### Whisper

### Auto Reeling and Tired

### Display Reeling/Tired Status in Chat

## Miscellaneous

### Enable Blind Rolls fdor Players

### Player Chat Commands are Private

### Portrait Path

### Set Roll Mode based on Ctrl Key

### Show Confirmation Roll Dialog

### Use Modify Dice + Adds Rule

### Show Effect Modifier Popup

### Quick Sheet

