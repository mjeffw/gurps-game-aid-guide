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
### Show Item Image in Character Sheet
Allows you to turn on or off an image associated with Traits, Skills, Spells, or Equipment on the character sheet. 

A cool way to show the image of a magic item directly on the sheet, for example.
### Color Character Sheet
Allows you to selectively override the colors of the Full (GCS) Character Sheet.
### Resource Tracker Manager
Allows you to create and apply standard [[Resource Tracker]] instances to character sheets. Resource trackers provide the user with a way to track non-standard values and pools such as Energy Reserve for the GURPS magic system or shield damage, etc.
### Show Document Debug Info
When checked, each character sheet will display a Debug icon in the title bar. Clicking this will so the data model of that actor. This is primarily of interest to users who want to write macros to automate some piece of functionality.
### Use Quintessence
If checked, this adds the Quintessence attribute and adds a Quintessence Points Resource Tracker to all characters. 

_This functionality will eventually be replaced by implementing custom attributes in GGA v1.0+._



