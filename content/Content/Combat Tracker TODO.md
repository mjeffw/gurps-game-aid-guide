
> [!TODO] ToDo
> Review for completeness

Combat Tracker enhancements make it easier for the GM to handle each combatant's rolls in the Foundry Combat Tracker.

To use, just click the button to open the menu with the quick rolls selected for that actor. When opened for the first time, you will see this:

![image](https://github.com/user-attachments/assets/6e7850b4-d958-4b03-8027-29917e87c560)
 
* **Checks**: the secondary checks for the Actor, including base damage.
* **Defenses**: the selected defenses for the Actor. On default configuration, only Dodge is selected.
* **Attributes**: The main attributes checks for the Actor, including Perception and Will rolls.
 
These options can be configured in [[Miscellaneous Settings#Use Quick Roll Button]]: 

![image](https://github.com/user-attachments/assets/dd2e0e47-c544-4b7a-acde-c33402dbb4e5)

![image](https://github.com/user-attachments/assets/311731d3-e449-421d-98d2-6c31efa57c1f)
### Making blind rolls
Click on the Eye icon on the menu to toggle between regular and blind rolls. For GMs, the default behavior is blind rolls.
### Adding new Rolls
To add new rolls to Quick Roll, open the Actor sheet from the Token or from the Actor list, and on the correspondent Actor Component (or if you're using Foundry Items, the Actor Item) select the `Add to Quick Roll` option for that component/item.

Please note:

* When opening the Sheet from the **Token**, you will change only the Quick Rolls for _that_ token.
* When opening the Sheet from the **Actor**, you will change the Quick Rolls for **all** tokens _linked_ to that actor.

![GGAQuickRoll](https://github.com/user-attachments/assets/0fe38d83-3c71-4517-991b-9537d13d45a6) [ ![GGAQuickRoll](https://github.com/user-attachments/assets/0fe38d83-3c71-4517-991b-9537d13d45a6) ](https://private-user-images.githubusercontent.com/11915032/385483684-0fe38d83-3c71-4517-991b-9537d13d45a6.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mzg0MjU3NjYsIm5iZiI6MTczODQyNTQ2NiwicGF0aCI6Ii8xMTkxNTAzMi8zODU0ODM2ODQtMGZlMzhkODMtM2M3MS00NTE3LTk5MWItOTUzN2QxM2Q0NWE2LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTAyMDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwMjAxVDE1NTc0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTg1YzUxMzU2N2Y4MGQ2ZWZlMzdlNWZiY2U3MGEwZWNiODVlMTU1NjM0MmY1ZDhmYWIyMTlkMThkMWI4NGMwNzUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.ADkaRJbm1mU2gXV3MQKZo1hmHwpGY7fd9bOxly9RJhE) [ ](https://private-user-images.githubusercontent.com/11915032/385483684-0fe38d83-3c71-4517-991b-9537d13d45a6.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mzg0MjU3NjYsIm5iZiI6MTczODQyNTQ2NiwicGF0aCI6Ii8xMTkxNTAzMi8zODU0ODM2ODQtMGZlMzhkODMtM2M3MS00NTE3LTk5MWItOTUzN2QxM2Q0NWE2LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTAyMDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwMjAxVDE1NTc0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTg1YzUxMzU2N2Y4MGQ2ZWZlMzdlNWZiY2U3MGEwZWNiODVlMTU1NjM0MmY1ZDhmYWIyMTlkMThkMWI4NGMwNzUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.ADkaRJbm1mU2gXV3MQKZo1hmHwpGY7fd9bOxly9RJhE)

When you add a melee attack to Quick Roll, system will add:

* The Melee Attack
* The Block and Parry for that Attack, if they exist.

Also, for Melee and Ranged attacks, hold `crtl` key before click to roll for damage instead the attack roll:

![GGAQuickRollDamage](https://github.com/user-attachments/assets/ac6bddba-59e4-421f-85d1-8315d07d8f42) [ ![GGAQuickRollDamage](https://github.com/user-attachments/assets/ac6bddba-59e4-421f-85d1-8315d07d8f42) ](https://private-user-images.githubusercontent.com/11915032/385485058-ac6bddba-59e4-421f-85d1-8315d07d8f42.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mzg0MjU3NjYsIm5iZiI6MTczODQyNTQ2NiwicGF0aCI6Ii8xMTkxNTAzMi8zODU0ODUwNTgtYWM2YmRkYmEtNTllNC00MjFmLTg1ZDEtODMxNWQwN2Q4ZjQyLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTAyMDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwMjAxVDE1NTc0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTYyN2E0NzI0NGJiMDBlZjMzNDExYjQxY2ZiZDFlOTQwOTA0Y2YwNjE1YmZmNTMwOGYwM2RmNjMxOGUxYTE1ODImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.JxZog7DSlwSmiqZoBvFMuOlhombG6CpcGAgXgheH8Mw) [ ](https://private-user-images.githubusercontent.com/11915032/385485058-ac6bddba-59e4-421f-85d1-8315d07d8f42.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mzg0MjU3NjYsIm5iZiI6MTczODQyNTQ2NiwicGF0aCI6Ii8xMTkxNTAzMi8zODU0ODUwNTgtYWM2YmRkYmEtNTllNC00MjFmLTg1ZDEtODMxNWQwN2Q4ZjQyLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTAyMDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwMjAxVDE1NTc0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTYyN2E0NzI0NGJiMDBlZjMzNDExYjQxY2ZiZDFlOTQwOTA0Y2YwNjE1YmZmNTMwOGYwM2RmNjMxOGUxYTE1ODImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.JxZog7DSlwSmiqZoBvFMuOlhombG6CpcGAgXgheH8Mw)

### Adding OTF

Just add the Component or the Item to the Quick Roll. System will search for OTFs on the `Notes` field for skills, spells and traits:

![GGAQuickRollOTF](https://github.com/user-attachments/assets/988a25f9-f88b-47ee-a9d3-c22b34f54291) [ ![GGAQuickRollOTF](https://github.com/user-attachments/assets/988a25f9-f88b-47ee-a9d3-c22b34f54291) ](https://private-user-images.githubusercontent.com/11915032/385488047-988a25f9-f88b-47ee-a9d3-c22b34f54291.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mzg0MjU3NjYsIm5iZiI6MTczODQyNTQ2NiwicGF0aCI6Ii8xMTkxNTAzMi8zODU0ODgwNDctOTg4YTI1ZjktZjg4Yi00N2VlLWE5ZDMtYzIyYjM0ZjU0MjkxLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTAyMDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwMjAxVDE1NTc0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWY5NTllMjg2M2Q1Y2JhN2UxZjBmMTJiMGNiMzUyOGI1YjUzNzdlZTQ0OTRlYTUxY2ZiYTc1ZTUzNDUzNGZmZTUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.__T4joQA4PdlB6uqP5G7gQ_YLA2pwRrcyrXHI4UicR0) [ ](https://private-user-images.githubusercontent.com/11915032/385488047-988a25f9-f88b-47ee-a9d3-c22b34f54291.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3Mzg0MjU3NjYsIm5iZiI6MTczODQyNTQ2NiwicGF0aCI6Ii8xMTkxNTAzMi8zODU0ODgwNDctOTg4YTI1ZjktZjg4Yi00N2VlLWE5ZDMtYzIyYjM0ZjU0MjkxLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTAyMDElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwMjAxVDE1NTc0NlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWY5NTllMjg2M2Q1Y2JhN2UxZjBmMTJiMGNiMzUyOGI1YjUzNzdlZTQ0OTRlYTUxY2ZiYTc1ZTUzNDUzNGZmZTUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.__T4joQA4PdlB6uqP5G7gQ_YLA2pwRrcyrXHI4UicR0)


### Set Maneuver 

This makes it easier for the GM to manage each combatant's maneuvers in the Foundry's Combat Tracker.
 
It's simple to use, just click on the button to select a maneuver for the combatant. To remove the selected maneuver, just right-click.

This button is visible only after that token rolled for initiative. The initiative number is now in the Token's image tooltip.

![GGAManeuverButton](https://github.com/user-attachments/assets/04cb2406-a452-4502-ac1d-8726262a9ae8) 

The tooltip gives tips about the selected maneuver:

* The token's maximum movement - calculated from current move vs the selected maneuver
* Whether the token can attack
* Whether the token can defend
* 


