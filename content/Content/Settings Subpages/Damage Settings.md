These settings control how the [[Apply Damage Dialog ✓]] (ADD) works.
### Restrict ADD to GM
If checked, only the GM can view or use the Apply Damage Dialog. If a player tries to apply damage to another character will get a warning.
> [!NOTE] Recommended Value
> Checked
### Simple ADD
If checked, only the simple version of the ADD will be displayed. The user can change the injury value and the resource pool (e.g., HP or FP) to reduce, but nothing else. This might be useful in a game where the players want to calculate their own injury values.
![[Pasted image 20260719173825.png]]
### Default Hit Location
Sets the default hit location used to apply damage. This value may be overridden in the (non-Simple) ADD.
- **Torso**
- **Random**
### Armor Divisors
If checked, the target's DR will be adjusted by the armor divisor of the attack. So, for instance, if a damage roll of `3d-1(2) imp` is applied to a target with DR 6, that target's DR will be divided by 2 for this attack.
> [!NOTE] Recommended Value
> Checked
### Blunt Trauma
If checked, use the Blunt Trauma rules to calculate damage on flexible armor.
> [!NOTE] Recommended Value
> Checked
### Location Wounding Modifiers
If checked, apply Wounding Modifiers based on damage type and Hit Location when calculating injury.
> [!NOTE] Recommended Value
> Checked
### Show the Math
If checked, all math involved in calculating injury by the ADD will be displayed in the Damage chat message.
> [!NOTE] Recommended Value
> Checked

![[Pasted image 20260719174618.png]]
_Figure: A Damage chat message with "Show the Math" checked._
### Conditional Injury
If checked, replaces Hit Points from the game as a way of tracking injury with the system "Conditional Injury" from Pyramid \#3/120.
### Body Hits
If checked, use the rules from High Tech p.162: Piercing, Impaling, and Tight-Bean Burning damage dealt to the Torso is capped at 2 x Max HP, and there is an additional 1 in 6 chance of hitting the vitals when targeting the Torso.
### Default Action for ADD
This setting determines (by default) whether there is a chat message associated with applying damage to a character that is visible to everyone. 

This might matter to a gaming group because if you see how much injury from a given damage roll was applied, a player might be able to reverse engineer the amount of DR, any Injury Tolerance, or Vulnerabilities of the target.

- **Apply Damage**: Everyone can see the amount of damage applied, in a chat message.
- **Apply Damage (Quietly)**: No one but the GM and the owner can see the chat message.
- **Target**: Applies publicly to Player Characters (any combatant owned by someone other than the GM) and privately to NPCs (characters owned only by the GM)

> [!NOTE] Recommended Value
> 'Target'
