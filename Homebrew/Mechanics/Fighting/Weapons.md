As stated in Fighting.md (3) the weapons all gain different buffs and debuffs making builds more relevant, but also flavored.

Those buffs got a scaling from range about 5 points. But I will immediately calculate it to the actual mod. For this the baseline is just the normal sword in DnD called Long Sword.

## Buffs
### Parry DC Buff
This is indicator about how hard it is to actually get the parry done. This is mainly influenced by the weapons size and attack angle.

### Parry Buff
This is the Buff of your parry weapon you can add to your Role and buffs on a parry. This is mainly influenced by the weapons properties, so size mainly.

### Stance-Breaking Damage
This is the Damage buff applied if you hit someone want to parry/block you. This is based on weight of the weapon. This does only affect the stamina drain not the actual damage if you hit the opponent!

### Block Buff
This is the Buff of your block weapon you can add to your Role and buffs on a block. This is mainly influenced by the weapons properties, so size and resistance mainly.

### Initiative-Buff
If your weapon is really heavy it is likely to slow you down. To simulate that you get a buff or debuff depending on your weapons size and weight. So clunky weapons like staffs even than slow you down if they are more light weight.

## Overview

| Weapon               | Wield  | Init |Dodge-Difficulty | Parry (Defense) | Parry (attack) | Block (Defense) | Block (attack) | Damage |
| ------------------- | ------ | ---: | --:|-------: | ----: | ----: | ---------: | ------: |
| Keule               | single |   -1 |  0 |    -1 |    -1 |     0 |         +1 | 1d6
| Dolch               | single |   +3 |  -2 |    +1 |    -2 |    -2 |         -2 | 1d6
| Handaxt             | single |   +1 |  -1 |    -1 |    -1 |     0 |         +1 | 1d6
| Wurfspeer           | single |   +1 |   |    +2 |     0 |    -1 |          0 | 1d6
| Leichter Hammer     | single |    0 |  -1 |    -2 |    -1 |    +1 |         +1 | 1d6
| Streitkolben        | single |   -1 |  0 |    -2 |    -2 |    +2 |         +2 | 1d8
| Sichel              | single |   +2 | -2  |    -2 |    -2 |    -2 |         -1 | 1d6
| Wurfpfeil           | single |   +3 |   |    -3 |    -3 |    -3 |         -3 | 1d6
| Schleuder           | single |   +3 |   |    -3 |    -3 |    -3 |         -3 | 1d6
| Morgenstern         | single |   -2 |  +1 |    -3 |    -2 |     0 |         +3 | 1d8
| Rapier              | single |   +2 |  0 |    +3 |    +3 |    -2 |         -2 | 1d6
| Krummsäbel          | single |   +2 |   0|    +1 |    +1 |     0 |          0 | 1d6
| Kurzschwert         | single |   +2 |   0|    +2 |    +1 |     0 |          0 | 1d6
| Blasrohr            | single |   +3 |   |    -3 |    -3 |    -3 |         -3 | 1d6
| Kampfstab           | single |    0 |   +1|    +2 |    +2 |    +2 |          0 | 1d6
| Kampfstab           | double |   -1 |   +2|    +3 |    +3 |    +3 |         +1 | 2d4
| Speer               | single |   +1 |+1   |    +2 |    +1 |     0 |          0 | 1d8
| Speer               | double |    0 | +2  |    +3 |    +2 |    +1 |         +1 | 1d4+1d6
| Streitaxt           | single |   -1 |  +1 |    -1 |     0 |    +1 |         +2 | 1d8
| Streitaxt           | double |   -2 |  +2 |     0 |    +1 |    +2 |         +3 | 1d4+1d6
| Langschwert         | single |    0 |   +1|     0 |     0 |     0 |          0 | 1d6
| Langschwert         | double |   -1 |  +2 |    +1 |    +2 |    +2 |         +1 | 2d4
| Kriegshammer        | single |   -2 | +1  |    -1 |     0 |    +2 |         +3 | 1d8
| Kriegshammer        | double |   -3 |  +2 |     0 |    +1 |    +3 |         +3 | 1d6+1d4
| Großer Knüppel      | double |   -2 |   +1|    -1 |     0 |    +2 |         +2 | 1d8
| Leichte Armbrust    | double |   -2 |   |    -3 |    -3 |    -3 |         -3 | 1d6
| Hellebarde/Pike          | double |   -3 |+3   |    +1 |    +2 |    +2 |         +3 | 1d6
| Schwere Armbrust    | double |   -3 |   |    -3 |    -3 |    -3 |         -3 | 1d8
| Kurzbogen           | double | +1   |   |    -3 |    -3 |    -3 |         -3 | 1d6
| Langbogen           | double |    0 |   |    -3 |    -3 |    -3 |         -3 | 1d8

## Special Weapons
### Shield

A shield does not deal any damage on Attack! Therefore your Target needs to do an STR-Check $\text{DC} = 10 + \text{Your STR-Mod} - \text{enenies STR-Mod} + \text{Your Prof-Mod} - \text{enenies Prof-Mod}$. If it fails that check it falls to the ground and so gets the on-the-ground-mod what will be discussed in Buffs and debuffs Markdown as soon I wrote that! In case your Enemy tries to parry or block that attack, throw a normal 1d6 for Block or Parry Energy drain!

| Schild           | Typ     | Init | Parry DC | Parry | Block | Stance Damage |
| ---------------- | ------- | ---: | -------: | ----: | ----: | ------------: |
| Buckler          | Special |   +1 |       +1 |    +1 |     0 |             0 |
| Schild  | Special |    0 |       +2 |    +2 |    +1 |            +1 |
| Großschild | Special |   -1 |       +2 |    +2 |    +2 |            +2 |
| Turmschild¹       | Special |   -3 |       +3 |    +1 |    +3 |            +2 |

¹: If blinded your blocking has no disadvantage.

### Natural Weapons

As your movement is not blocked or slowed in any way all checks whatfore figners or arms are useful the DC becomes 1 lower. This also applies to dodges.

The weapons themself you find in Classes and Races markdowns. 

If you or your dm want you can't wield a weapon with your paws like a tabaxi normally couldn't, your natural weapons may get a little stronger, scaling and/or counting as magic, as you and your dm decide.