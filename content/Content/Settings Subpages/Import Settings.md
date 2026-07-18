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