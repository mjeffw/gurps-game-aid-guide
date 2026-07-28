## How do tags work?
Tags are identifications that allow you to cross-reference the roll with their existing "modifiers":
* In the _effect modifier_, you add the tags that identify that bonus or penalty. Ex. `+1 to camouflage #hide`
* In the skill, spell, attack, defense or damage (the _source of the roll_), you tell the system which tags it should look for before making the roll. Ex. `hide, scout`

Using the example above, using an Actor which have the **Camouflage** skill and the _Cloth Armor_ equipment:

On Actor Component or Item editor for the `Camouflage` skill, add on the `Modifier Tags` field the tag `hide`:

![image](https://github.com/user-attachments/assets/600c0089-dfe2-4245-8a13-8cf8bfca7fba)

On Actor Component or Item editor for the `Cloth Armor` equipment, inside `Modifiers` tab, add the following modifier: `+1 to camouflage #hide`

![image](https://github.com/user-attachments/assets/19bce9e4-5b1a-4511-964f-c5efbd2c1a51)

Click on the Actor, you will see on the Effect Modifiers Popout:

![image](https://github.com/user-attachments/assets/4b2b40e1-d110-478e-9356-1ba6393b33cb)

Click to roll `Camouflage`. On the Modifier Bucket you will see the modifier automatically selected:

![image](https://github.com/user-attachments/assets/28bc4cc7-937f-445d-90ef-72e2f53becc5)

## Can I create custom modifiers?
Yes, for example you can create a custom modifier on the Modifier Effects Popout, clicking on button (+):

![image](https://github.com/user-attachments/assets/045b4d43-6bb7-4d79-b010-2b23efa6518f)

For example, you can use the reserved `#skill` tag to create modifiers to all skills (more on that later). On the previous example, add the `+1 divine guidance #skill` on the popout:

![image](https://github.com/user-attachments/assets/d2a3d2e0-d03d-4a7e-b750-f28c0431035a)

## And about Active Effects?
Just add the #tag you want on the Active Modifier you want to create. For example, if you want to create the `-2 to defenses from bad foot`, on the Active Effects you create the modifier, against the `system.conditions.usermods` and adding the `#defense` tag to your modifier:

![image](https://github.com/user-attachments/assets/ee34996a-694d-4c0d-842c-0731e276dba4)

When you click on any defense you will see the modifier, if the Active Effect is enabled:

![image](https://github.com/user-attachments/assets/24e0ab44-cc59-4f97-8975-cc0a3f4192c5)

Use the following paths for modifiers:
* `system.conditions.usermods`: for modifiers which affect actor own traits
* `system.conditions.target.modifiers`: for modifiers which after actor own traits related to his target (for example, ranged penalties)

With this in mind, the options for saving modifiers are:
* In the trait that originated the modifier, within the Actor Sheet.
* In the `Conditional Modifiers` section of the Actor's Sheet
* In the `Reaction Modifiers` section of the Actor's Sheet
* In the `Effect Modifiers` popup of the system.
* In the `Active Effects` created effect. 

## Reserved Tags 
Reserved tags are special tags destined for rolls that do not have an item or actor component to represent, such as attribute tests (ST, Will, etc.), character checks (vision, fright check, etc.), or skill/spell groups.

In the two examples above, we use two reserved tags: `#hit` and `#defense`. The first will be used on all ranged/melee attacks, the second, on all defense rolls. Some of the reserved tags on the system:

* `#all` - All Rolls
* `#damage` - All Damage Rolls
* `#attribute` - All attribute Rolls
* `#iq` - All IQ rolls
* `#per` - All Perception rolls
* `#fright` - All Fright Check rolls
* `#control` - All Control Rolls
* `#melee` - All Melee Attack Rolls
* `#dodge` - All Dodge Rolls
* `#skill` - All Skill Rolls
* `#spell` - All Spell Rolls. Also you can check the `Use Spell College as Tags` on settings to use the Spell College as tag (ex. #fire for fire spells)
* `#combat` - Only during combat
* `#no_combat` - Only outside combat

For the **complete** list and if you want change them, all reserved tags can be found in the Foundry settings:

![image](https://github.com/user-attachments/assets/78e12732-7873-4c1f-be4c-c4d7904bfb36)

* You can change or remove default reserved tags.
* On this screen you can also disable auto add tagged modifiers

## Modifier with tags format
The format is `<modifier> <description> <#tag1> <#tag2>...` 
* You can add as many tags as you want. 
* Tags accept only letters, numbers and underscores. `#foo` is good, `#b@r` is bad. 

Some examples:
* `+1 from first aid kit #heal`
* `+2 to elemental spells #fire #water #earth #air`
* `-1 broken aim #combat #ranged`

### Under the hood: the modifier source
If you debug the modifiers you will see something like this `+1 to hit #hit @custom`. The `@xxxx` is a internal tag on the system to indicate the modifier origin. Some examples are `@man:aoa_double` (the modifier origin is from the AoA Double maneuver), `@combatmod` (the modifier origin is from combat), @custom (the modifier is user created), and many others.

Please do not change the `@tags` using macros ou Active Effects, they are intended for internal use only. We will do not support bugs or macros which change these internal tags.

## The `Effect Modifiers` popup
Use this window to create custom modifiers and to see the list of Actor modifiers. **Only the modifiers listed here** will be searched for the roll and be added automatically if they have the correct tags.

![image](https://github.com/user-attachments/assets/9d6b0ff1-d910-42fc-b45d-0998bf7775cb)

This window shows the following information:
* The modifier's description.
* The modifier's origin or the source of the roll (calculated by the system).
* The modifier's tag list.

Modifiers with a "**custom**" origin are those created by the user. 
* To create a new custom modifier, use the (+) button.
* To update the list, use the **refresh** button.

### Deleting modifiers
* To delete a custom modifier, simply right-click on it in the popup.
* To delete a saved modifier, on right-click, system will open the Item or the Sheet (for actor components)
* To delete all modifiers, use the delete button. Note that if you click the `refresh` button, all modifiers saved on the player's sheet will be added again.

Note: Modifiers added by Active Effects cannot be deleted via the Effect Modifiers popup. The Active Effect must be disabled or deleted from the character. You can always remove any modifier regardless of where it came from via the Modifier Bucket window.

