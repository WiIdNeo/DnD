# Combat System for DnD Homebrew

Many aspects of DnD's standard rules feel too light, too generic, or
tactically flat. The goal of this system is to make combat more realistic and
tactically demanding: a bandit should feel different from a dragon — not just
through more HP, but through different decisions made during the fight.

**Core idea:** Real physical resilience barely increases with level — a human
dies from an arrow to the eye regardless of experience. What actually
increases is technique and anticipation. This isn't reflected by more HP, but
by better active defense — now fueled by a shared, **Token
pool**.

If not stated differently, the original DnD fighting rules apply. This is a
theoretical concept, not yet playtested. Raise an issue if you spot a problem!

---

## 1. Core Mechanic: Ranged vs. Melee

| Distance | DC |
| ---------: | --------------: |
|      0.5 m |               2 |
|        5 m |               3 |
|       10 m |               4 |
|       20 m |               6 |
|       30 m |               8 |
|       40 m |              10 |
|       50 m |              12 |
|       75 m |              15 |
|      100 m |              18 |
|      125 m |              20 |

> **Exception — Called Shots:** Precise hits on small target zones (eye,
> throat) remain uncertain even at close range. The attacker rolls an
> additional precision check, only as a deliberate special action. DM decides
> how much harder called shots are — smaller zone = harder, and size
> differences between combatants (e.g. a halfling aiming for a giant's eye)
> may raise the difficulty or require a prior skill check.

---

## 2. Attributes

### STR
Harder hits → harder to parry/block, easier to break the opponent's stance.
Own blocks are more resilient.

### DEX
Faster movement → higher initiative, better parries. Arrow shots are easier
to dodge. Governing stat for finesse weapons and ranged combat.

### CON
Increases HP, and decreases stamina drain in longer fights. 

**Governing stat per weapon:** STR for most melee weapons, DEX for finesse
weapons (dagger, rapier) and ranged combat.

---

## 3. Weapon Table

Weapons grant different buffs/debuffs to checks and properties, making
weapon choice tactically important. Full table lives in `Weapons.md`.

---

## 4. Magic

Most spells require line of sight and (for precision effects) anatomical
knowledge of the target. Projectile spells work like physical ranged
attacks: the defender gets a normal Dodge/Block/Parry check against them.

---

## 5. Tokens 

### 5.1 Pool

**Here may create a CON-Based Table to manipulate the reduction**

Every combatant gets a fresh pool at the **start of combat**, sized per
round rather than per fight:

$$\text{Tokens}(\text{Round } n) = \max\big(\text{Floor},\ 10 - (n - 1)\big)$$

- Round 1: 10 tokens. Round 2: 9. Round 3: 8. … and so on.
- **Floor = 0** by default — the pool can fully run dry in long fights,
  making late rounds progressively more luck-driven instead of tactical.
  This is intentional: it matches a setting where weapons are extremely
  lethal and long fights should feel increasingly desperate.
- **Feats/Buffs** may raise the Floor (e.g. "never below 2") or slow the
  decay (e.g. "−1 every 2 rounds instead of every round"). This is your
  primary progression lever going forward — no separate Stamina formula
  needed.
- If your Token Pool at the end of the round is higher than your new would be you gain the difference in addition to the new pool's size.

### 5.2 Spending — both sides bid on their own roll

For every individual attack/defense exchange, **both combatants** secretly
commit a number of tokens from their current round's pool, then reveal
simultaneously and roll:

- **Attacker tokens** add directly to the attacker's own d20 roll.
- **Defender tokens** add directly to the defender's own d20 roll.

Tokens are **spent immediately on reveal, win or lose** — bidding is a real
commitment, not a guaranteed bonus. 1 token = +1 flat, no conversion table
needed.

This restores the bluffing tension of committing a resource before knowing
the opponent's commitment — without requiring full-round scripting for the
whole party. Each exchange is resolved independently, in normal turn order,
as one opposed roll (see Section 6).

---

## 6. Opposed Roll (core resolution)

Attacker and defender both roll 1d20 and add their own modifiers. Higher
total wins the exchange.

$$\text{Attack Roll} = 1d20 + \text{Attacker-Prof} + \text{Attribute-Mod(weapon)} + \text{Speed Bonus}_{\text{Atk}} + \text{Attacker-Tokens}$$

$$\text{Defense Roll} = 1d20 + \text{Defender-Prof} + \text{Stance-Mod} + \text{Attribute-Mod(stance)} + \text{Defender-Tokens}$$

- **Stance-Mod** is whichever Dodge/Block/Parry modifier applies — see
  Section 7, note that the signs there are written for *this* roll-based
  format (higher Stance-Mod always helps the defender).
- **Attribute-Mod(weapon)** for the attacker is the weapon's governing stat
  (STR for most melee, DEX for finesse/ranged, see Section 2).
- **Attribute-Mod(stance)** for the defender: DEX for Dodge/Parry, STR for
  Block.
- A natural 20 always wins the roll it's part of; a natural 1 always loses
  it, regardless of totals.
- **Tie:** defender wins (benefit of the doubt goes to defense).

### Speed Bonus (replaces the old DC-tier approach)

Only increases, can't decrease.

| Initiative Difference | Speed Bonus (faster side only) |
|---|---|
| 0–2 | +0 |
| 3–5 | +1 |
| 6–8 | +2 |
| 9–11 | +3 |
| 12–14 | +4 |
| 15–17 | +5 |
| 18–20 | +6 |
| ... | ... |

A nat1/nat20 only affects position in the action queue beyond its roll
effect above; the initiative difference itself still updates according to
Buffs.

---

## 7. Defense Options

### 7.1 Dodge

DEX is already represented via the Attribute-Mod and Speed Bonus (Section
6). The Stance-Mod is a **malus** — the more ground you need to cover, the
harder it is to actually pull off:

$$\text{Stance-Mod (Dodge)} = -\big(\text{DC(Distance out of the AoE)} \times \text{Reaction Time Mod}\big)$$

| Way out of the AoE | DC |
|-|-|
| 0.5 m | 1 |
| 1 m | 2 |
| 2 m | 4 |
| 3 m | 9 |
| 4 m | 16 |
| 5 m | 25 |
| 6 m | 36 |

(Below 2 m: y = 2x. At 2 m or higher: y = x².)

| Tell | Reaction Time Mod |
|---|---|
| None (instant) | ×(5/3) |
| Short | ×(4/3) |
| Normal | ×1.0 |
| Slow | ×(2/3) |

Dodges backwards are always harder: −1. See the Weapon Table for typical
attack angle/reach, which determines how small the escape AoE can be.

- **Win:** 0 damage.
- **Lose:** full damage.

### 7.2 Block

Stance-Mod: $+(2 + \text{Weapon Mod})$ — added to your Defense Roll.

Block is all-or-nothing on the outcome, but **which** way it fails depends
on the attacking weapon:

- **Win the opposed roll:** full absorb, 0 damage.
- **Lose the opposed roll:** your stance breaks, per the matrix below.

**Stance-Break Matrix** (Attacker weapon **weight** × your **block tool
size**, determines base difficulty; attacker weapon **type** determines the
failure consequence):

| Attacker weight ↓ / Block tool → | Large (Shield) | Medium (Sword/Axe) | Small (Dagger) |
|---|---|---|---|
| Light / Arrow | Easy to block | Neutral | Hard (small surface, easy to miss) |
| Medium (sword, axe) | Neutral | Neutral | Malus (size mismatch) |
| Heavy (hammer, greatsword) | Malus, but blockable | Clear malus | Barely blockable |

| Attacker weapon type | Consequence on failed Block |
|---|---|
| **Blunt** | Stagger/knockdown — you're prone or open next action |
| **Sharp** | Damage leaks through, reduced but real |

### 7.3 Parry

Stance-Mod: $(\text{Weapon Mod} - 2)$ — added to your Defense Roll. Can be a
malus if your Weapon Mod is below 2, reflecting that a good parrying weapon
is what makes this option viable at all.

- **Win the opposed roll:** 0 damage + a guaranteed free counterattack
  (cannot be evaded, no reaction from the opponent). Counter damage is
  reduced by the opponent's Prof-Mod.
- **Lose the opposed roll:** you take the full hit **and** you're left
  open — the attacker gets one additional guaranteed counter-hit (same
  "cannot be evaded" logic, mirrored). High risk, high reward on both
  sides.

---

## 8. Damage

$$\text{Damage} = \max\left(1,\ 1d6 + \text{Prof-Mod} + \text{Stat-Mod}\right)$$

- **Prof-Mod** unchanged (+2 to +6) — carries the level curve.
- **Stat-Mod** (weapon's governing stat) full weight.
- Minimum 1 damage on any hit, regardless of negative modifiers.


### Rounding Rule
Standard 0.5 → round up, but reduce the base value by 0.0.7 first (so x.5
averages effectively round down, e.g. 1d6 average 3.5 → 3.43 → 3).

---

## 9. AC & Initiative

### Initiative
Still determines turn order. The difference between two combatants'
initiative values also grants the faster side a Speed Bonus on the opposed
roll (Section 6) — no separate reaction gate roll.

### AC
Not binary hit/miss, but a damage modifier:

$$\text{Mod} = \frac{1}{AC/10}$$

AC 10 = neutral (×1), AC 20 = ×0.5 (half damage), AC 5 = ×2 (double damage).
Full avoidance remains reserved for active reactions (Block/Parry/Dodge).

---

## 10. Attack Zones

Base idea: specific body parts are more penetrating than others. A hit to
the arm or foot hampers movement but deals normal-to-low damage; a hit to
the head is dangerous, and a hit to ear/eye can be immediate death. Since
base damage here is low (~3.5 + mods), a vital-zone hit may grant a bonus
1d4–1d8 depending on zone, at DM discretion. High DC is intended for called
shots so fights don't become an "eye-shot simulator."

---

## 11. Worked Example: Opposed Roll with Token Bidding

**Setup:** A (Prof +4, STR-Mod +2, sword) attacks B (Prof +3, DEX-Mod +1).
B chooses to Parry. Weapon Mod for B's parrying weapon: +1. Same
initiative this round → Speed Bonus is +0 for both. Round 3, both have max
8 tokens available.

- Both secretly bid tokens: A bids 3, B bids 5. Reveal.
- **Attack Roll** = 1d20 + 4 (Prof) + 2 (STR-Mod) + 0 (Speed) + 3 (Tokens)
  → rolls a 11 → total **20**
- **Defense Roll** = 1d20 + 3 (Prof) + (1 − 2) (Parry Stance-Mod) + 1
  (DEX-Mod) + 0 (Speed) + 5 (Tokens) → rolls a 14 → total **22**
- All 3 and 5 tokens are spent regardless of outcome.
- B's 22 beats A's 20 → **B wins the Parry**: 0 damage, plus a guaranteed
  free counterattack against A (damage reduced by A's Prof-Mod).

If B had bid fewer tokens or rolled lower, losing the opposed roll means B
takes full damage *and* A gets an additional guaranteed counter-hit
(Section 7.3) — no proportional bleed-through math needed; the outcome is
always a clean win/lose per stance (Sections 7.1–7.3).

---


## 12. Buffs

Most buffs are covered in the separate `Buffs.md`.

### Advantage and Disadvantage
AC is just a damage modifier here, applied after the opposed roll decides
whether a hit lands at all (Section 6) — it doesn't touch the roll itself.
Advantage/Disadvantage therefore also don't touch the "hit die." If a
target is blinded, it isn't easier for you to aim —
it's harder for *them* to notice the attack. So Advantage/Disadvantage come
from specific Buffs/Debuffs and typically mean "best of two" on the damage
die, or disadvantage on a saving throw.

---

## 13. Dying

Reducing a creature's HP to 0 doesn't kill it immediately — it goes
unconscious. Wound severity then determines whether it starts dying and
needs care, or simply wakes up later. While down, a creature is helpless;
attacking an unconscious target allows an undefended finishing blow.

---

## 14. Opportunity Attacks

Handled as usual, but reactable unless the DM rules otherwise.

New type: entering someone's melee range grants them an opening-hit
opportunity at the normal Defensive Action DC with mod 0. If declared, you
can choose to react (treated as a normal out-of-sequence attack) or not
(you take the hit, or if they fail their DC they can't react to your next
action).

Leaving melee range grants a leaving attack:
- **Block/Parry:** as normal, but all distance moved before the block
  counts as moving backwards (×1.5).
- **Dodge:** if you guess the dodge timing, DC gets +1 per meter of the
  attacking weapon's melee reach. If you want the normal DC, you must walk
  backwards to the dodge point (×1.5 distance).

---

## 15. Disarming

**How to disarm:** either the foe critically fails (nat1) their
parry/block and drops the weapon, or you declare a disarm attempt — on a
hit, the foe makes an unbuffed d20 save against your damage (no HP damage
dealt). Losing the save drops the called-out weapon. Two-handed weapons
grant advantage on this save.

**What happens to the weapon:** it drops to the ground. For more detail,
the DM may estimate throw distance from the difference between the d20 and
the disarm damage, ×15 cm. After a disarm, anyone can pick up the weapon,
burning 5 ft of movement (DM discretion on feasibility by weight/size).
