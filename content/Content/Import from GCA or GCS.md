As mentioned in [[General Philosophy]], GGA versions prior to (the not yet released) v1.0.0 expect that you will create and maintain your characters in either GCS ([GURPS Character Sheet](https://gurpscharactersheet.com/)) or GCA ([GURPS Character Assistant](http://www.sjgames.com/gurps/characterassistant/)).

GGA has some editing functions, but due to the complexity of GURPS, it will leave all of the complex character creation rules to the applications that have been developed (for years!) specifically to handle them.

To use your characters in Foundry, it is best if you first create them in GCS or GCA, and then export them to Foundry. GMs can use the [[Mook Generator]] to create simple NPCs in Foundry.
## Settings
Some import functionality is configurable via [[Import Settings]].
## GCA
Creating a GGA character from a GCA file is multipart process:
- [[#Export from GCA|Export the character data]] from GCA.
- [[#Create an Actor]].
- [[#Import from GCS or GCA]].

Updating a GCA character:
- Update the character in GCA
- [[#Export from GCA|Export the character data]] from GCA.
- [[#Import from GCS or GCA]].
## GCS
Create a character from GCS is simpler:
- [[#Create an Actor]].
- [[#Import from GCS or GCA]].

Updating a GCS character:
- Update the character in GCS
- [[#Import from GCS _or_ GCA]].
# Export from GCA

> [!TODO]
> This section may be out-of-date.

![[Pasted image 20260720154642.png]]

To export from GCA, you must copy the export script from your Foundry data directory (or our online ZIP file) to the GCA “sheets” directory.

The export script is: `<Foundry Data Directory>/Data/systems/gurps/exportutils/export to Foundry VTT.gce`

Copy the export script into your GCA "sheets" directory.

Load the character, and select the menu options **File** -> **Export**. In the “Export Options” dialog, select “**Export to Foundry VTT.gce**” in the pulldown, and check the “**Custom file format**” box.

![[Pasted image 20260720155001.png]]

NOTE: You DO NOT need to change the File extension. You may leave it as “.TXT”.

Press “**OK**” and the “**Export File To…**” dialog will appear. Just press “**Save**”, and it will save the export right next to your character (just remember to check “Custom file format”!). For example, if the character file is named:

   `Franklin Dunne (Cowboy).gca4`

The export will be named:

   `Franklin Dunne (Cowboy).gca4.TXT`

You can save the file anywhere, but check out [[#Special Export Location]] for an added feature.
### Special Export Location
GGA has the ability to re-import characters without prompting for the file name if they are saved in a special location.

Find Foundry's “User Data Path”. You can see what it is by bringing up the **Configure** option on the main Foundry page.
![[Pasted image 20260720155610.png]]

Click the Configure button and read the value of the **User Data Path** option.

![[Pasted image 20260720155740.png]]

Open a file browser and navigate to the “User Data Path” directory. It will contain a “Data” subdirectory. Navigate into that. 

In “Data”, you will see the subdirectories “modules”, “systems” and “worlds” (and there could be more). Create a new directory here to store characters, and under that, you can create subdirectories for each of your worlds (if you want).

For example, you could create the subdirectory “characters” and under it, you create “homegame” and “tuesdays”.

And in this example, when you export a character from GCA or GCS, export it into the appropriate subdirectory:  

`C:/Documents/Personal/FoundryVTT/Data/characters/homegame` or  `C:/Documents/Personal/FoundryVTT/Data/characters/tuesdays`

After your initial import of the character (which will ask for a file location), GGA will be able to detect that the file is in a well known (and safe) location, and can re-import it without bringing up the file dialog.
# Create an Actor
"Actor" is Foundry terminology for things in the game that can act, such as characters, NPCs, animals, vehicles, etc. Whether you want to create an Actor directly in GGA (not fully supported yet) or import a character from GCS/GCA, the first thing you will do is create an Actor.

First, click on the Actors tab on the right-hand toolbar:
![[Pasted image 20260720153113.png]]

Then click on the **Create Actor** button:
![[Pasted image 20260720153151.png]]

**Name** the actor and set the **Type**.
![[Pasted image 20260720153251.png]]

Generally, you should stick with type = "character". Entering the name at this point is optional if you are going to import from GCS/GCA as the character name may be overridden based on the value of setting [[Import Settings#Ignore 'name' Attribute]]. Click the **Create** button. The default Actor sheet for this character will open.

![[Pasted image 20260720153535.png]]
_Figure: The empty Full (GCS) Actor sheet._

![[Pasted image 20260720153627.png]]
_Figure: An empty Modern Actor sheet._

# Import from GCS or GCA
Click the **Import** button in the titlebar of the Actor sheet window.
![[Pasted image 20260720154117.png]]
Click the **Choose File** button and select a GCS v5+ file _or_ the GCA export file you created using the steps in [[#Import from GCA]]. 

Only the latest GCS or GCA versions are typically supported. If GGA fails to import the character, try updating GCS or GCA to the latest version, then opening the character in this version and then saving/overwriting it (GCS) or re-exporting it (GCA).

Click **Import**. The empty Actor should now be replaced with the imported data.
# Use  Non-locally Hosted Import Dialog 
For either GCS or GCA, setting [[Import Settings#Use Non-locally Hosted Import Dialog]] to "checked" (✅) will enable GGA to remember the location of the GCS or GCA file after the first import for that session. From that point onwards, clicking Import will immediately import the character from that location without prompting you for it each time.

# Editing Within Foundry
While GGA provides limited editing of the character sheet, it does not do any calculations on the new information. The limited editing is mainly there so that you (or the player) can add [On-the-Fly formulas](https://github.com/crnormand/gurps/wiki/User-Guide-%E2%80%90-GURPS-4th-Edition-Game-Aid-for-Foundry-VTT-\(Unofficial\)#on-the-fly-formulas) and take notes (see [Player entered values](https://github.com/crnormand/gurps/wiki/User-Guide-%E2%80%90-GURPS-4th-Edition-Game-Aid-for-Foundry-VTT-\(Unofficial\)#player-entered-values)).