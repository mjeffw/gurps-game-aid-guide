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
