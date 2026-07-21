So now you have your characters in the world… but no one to fight. You need to create a few “mooks” (NPCs). You can use the character creation tools (GCA/GCS), but for “throw away” or low level NPCs, that seems to be overkill. Instead, you can create the “mooks” directly in our Game Aid. Check out our [“How to create NPCs”](https://www.youtube.com/watch?v=3Dyfjh0peLI) video. The GM can type “/mook” in the chat window to bring up the Mook Generator.

![[Pasted image 20260721122318.png]]

The GM can enter information, and press TAB to move to the next field. Once all of the information is entered, click “Test Mook” to verify that the data is correct, and if it is, the button will change to “Create Mook”. Click that to create the new Actor.

The Notes, Traits, Skills, Melee and Ranged values are parsed for **On-the-Fly** formulas.

Traits may be entered one per line, or separated by “**;**” or a combination of both.

Skills may be entered one per line, or separated by “**,**” or a combination of both.. Skills are parsed using the format:

   `<skill-name>-<number>`

The skill name may include any character except “**-**”. If you forget the “**-**”, or the value following the “**-**” is missing or not a number, an error will be added to the text when you try to create the mook.

Melee attacks must be entered one per line. Melee and ranged attacks are recognized if they follow 1 of 2 patterns:
```
Name (Skill #) damage-formula optional-attributes
Name (Skill Text) "damage text" optional-attributes
```
The name may include any character except “(“. As with Skills, if you do not follow the format, an error will be added to the text when you try to create the mook.

Melee attacks can also have the optional parameters, followed by “text”, separated by spaces. The “text” cannot contain spaces. The parameters are:

```
Reach/reach   
Usage/usage   
Parry/Parry   
ST/st  
Block/block
```

EX:  

```
Knife (12) 1d-2 cut reach c,1 st 10 usage stab  
Gaze (12) “Some non-rollable damage” reach c,1
```
NOTE: The “reach” value “c,1” does not contain a space.

The order after the damage formula does not matter.

Ranged attacks follow the same format as melee attacks. The can also include the optional parameters, followed by text, separated by spaces:

```
Acc/acc  
Rof/RoF/rof  
Rcl/rcl  
Usage/usage  
Range/range  
Shots/shots  
Bulk/bulk  
ST/st
```

Ex: `Long Range Rifle (12) 2d+1 pi range 50/100 bulk -5 acc 3`
Ex: `Longbow (12) 1d+1 imp range x1/x2.5 bulk -3 acc 4`

NOTE: The “range” value “50/100” does not contain a space, and can be of the form “xN” or “xN/xM” which indicates a ST based range.

Equipment follows the format:

   `<Item name>**;** X **;** $Y **;** Z lbs`

Where `<Item-name>` can contain spaces. X is the quantity of items. Y is the per-unit cost of the item, and Z is the weight in LBS. The format must include the “$” and “lbs” to be valid.

Equipment isn’t strictly necessary, since the melee and ranged attacks are described above, but some stat blocks include equipment, so we try to capture what we can.