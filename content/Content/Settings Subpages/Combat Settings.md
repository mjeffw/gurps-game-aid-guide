These settings modify how [[Combat TODO]] works and what options are available.
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
If checked, the additional aiming-related maneuvers and modifiers from "On Target" (Pyramid \#3/120) will be enabled.
### Maneuver Icon Visibility
Set who can see the maneuver chosen by the combatant. 
- **No One**
- **Owner and GM Only**
- **Everyone**
> [!NOTE] Recommended Value
> Everyone
### Maneuver Visibility Details
If the Maneuver is visible (see [[#Maneuver Icon Visibility]]), what, exactly, does everyone see (other than the GM and the player owner, who always sees **Full** detail)?
- **General**: The maneuver is shown without the maneuver option. So, for example, if a combatant chose _All-Out Attack: Double_, everyone besides the GM and Owner see _All-Out Attack_. All basic maneuvers are visible including _Feint_.
- **No Feint**: As **General** but _Feint_ will appear as _Attack_.
- **Full Detail**: The exact Maneuver and option chosen will be visible to everyone.
> [!NOTE] Recommended Value
> No Feint
### Maneuver Updates Move
If checked, the character's Move will be updated based on the maximum move allowed by the maneuver he has chosen.
> [!NOTE] Recommended Value
> Checked

![[Pasted image 20260719164530.png]]
_Figure: This character has chosen_ Aim _as his Maneuver; his move has been adjusted to the maximum of a Step._
### Allow Roll Based on Maneuver
Based on this setting, a Combat roll may be prevented or a warning shown if the roll should not be allowed based on the character's chosen maneuver.
- **Allow**: Allow the roll with no warning.
- **Warn**: Allow the roll, but warn the user.
- **Forbid**: Prevent the player from making the roll.
> [!NOTE] Recommended Value
> Warn

![[Pasted image 20260719165138.png]]
_Figure: If set to **Warn**: a Roll Confirmation dialog showing a warning that an Attack roll should not be made because the current Maneuver chosen is Aim._

![[Pasted image 20260719165229.png]]
_Figure: if set to **Forbid**: A popup warning showing that the Attack roll will be denied since the current Maneuver is Aim._
### Check for Targets Before Roll
Based on this setting, a Combat roll may be prevented or a warning shown if there is no target selected.
- **Allow**: Allow the roll with no warning.
- **Warn**: Allow the roll, but warn the user.
- **Forbid**: Prevent the player from making the roll.
> [!NOTE] Recommended Value
> Warn

![[Pasted image 20260719170200.png]]
_Figure: **Warn** is selected._

![[Pasted image 20260719170342.png]]
_Figure: **Forbid** is selected._
### Allow Roll Before Combat Starts
Based on this setting, a Combat roll may be prevented or a warning shown if the character is not in combat.
- **Allow**: Allow the roll with no warning.
- **Warn**: Allow the roll, but warn the user.
- **Forbid**: Prevent the player from making the roll.
> [!NOTE] Recommended Value
> Warn
### Use Max Actions Check
If enabled, check if each applicable combatant is attempting to use more actions than are allowed in a turn. For instance, if Attacking, normally only one attack roll may be made.
- **Disable**: Don't apply max action checks.
- **All Tokens in Combat**: Apply to all combatants.
- **All Tokens**: Apply to all characters in the scene.
> [!NOTE] Recommended Value
> All Tokens in Combat
### Allow Action After Max
If [[#Use Max Actions Check]] is being applied, this setting controls how the game will handle a combatant making too many actions in a turn.
- **None**
- **Warn**
- **Forbid**
> [!NOTE] Recommended Value
> Warn
### Automatically Add Cumulative Parry Penalties
If checked, the game will automatically add the cumulative parry penalty to any combatant affected by the [[#Use Max Actions Check]] setting.
> [!NOTE] Recommended Value
> Checked
### When to add Shock Effect
If a character would suffer Shock on an attack, this setting controls when the Shock effect is actually applied.
- **Immediately**: The Shock effect is applied immediately.
- **At Next Turn**: The Shock effect applies at the start of the affected character's next turn.
> [!NOTE] Recommended
> Immediately
