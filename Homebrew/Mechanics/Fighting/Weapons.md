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

| Weapon               | Wield  | Init | Parry DC | Parry | Block | Stance Dmg |
| ------------------- | ------ | ---: | -------: | ----: | ----: | ---------: | 
| Keule               | single |   -1 |       -1 |    -1 |     0 |         +1 | 
| Dolch               | single |   +3 |       +1 |    -2 |    -2 |         -2 | 
| Handaxt             | single |   +1 |       -1 |    -1 |     0 |         +1 | 
| Wurfspeer           | single |   +1 |       +2 |     0 |    -1 |          0 | 
| Leichter Hammer     | single |    0 |       -2 |    -1 |    +1 |         +1 |
| Streitkolben        | single |   -1 |       -2 |    -2 |    +2 |         +2 |
| Sichel              | single |   +2 |       -2 |    -2 |    -2 |         -1 |
| Wurfpfeil           | single |   +3 |       -3 |    -3 |    -3 |         -3 |
| Schleuder           | single |   +3 |       -3 |    -3 |    -3 |         -3 |
| Dreschflegel        | single |   -1 |       -3 |    -3 |    -2 |         +2 |
| Morgenstern         | single |   -2 |       -3 |    -2 |     0 |         +3 |
| Rapier              | single |   +2 |       +3 |    +3 |    -2 |         -2 |
| Krummsäbel          | single |   +2 |       +1 |    +1 |     0 |          0 |
| Kurzschwert         | single |   +2 |       +2 |    +1 |     0 |          0 |
| Kriegshacke         | single |    0 |       -2 |    -1 |     0 |         +2 |
| Peitsche            | single |   +3 |       -3 |    -3 |    -3 |         -3 |
| Blasrohr            | single |   +3 |       -3 |    -3 |    -3 |         -3 |
| Handarmbrust        | single |    0 |       -3 |    -3 |    -3 |         -3 |
| Netz                | single |    0 |       -3 |    -3 |    -3 |         -3 |
| Kampfstab           | single |    0 |       +2 |    +2 |    +2 |          0 |
| Kampfstab           | double |   -1 |       +3 |    +3 |    +3 |         +1 |
| Speer               | single |   +1 |       +2 |    +1 |     0 |          0 |
| Speer               | double |    0 |       +3 |    +2 |    +1 |         +1 |
| Streitaxt           | single |   -1 |       -1 |     0 |    +1 |         +2 |
| Streitaxt           | double |   -2 |        0 |    +1 |    +2 |         +3 |
| Langschwert         | single |    0 |        0 |     0 |     0 |          0 |
| Langschwert         | double |   -1 |       +1 |    +2 |    +2 |         +1 |
| Dreizack            | single |    0 |       +1 |     0 |     0 |          0 |
| Dreizack            | double |   -1 |       +2 |    +1 |    +1 |         +1 |
| Kriegshammer        | single |   -2 |       -1 |     0 |    +2 |         +3 |
| Kriegshammer        | double |   -3 |        0 |    +1 |    +3 |         +3 |
| Großer Knüppel      | double |   -2 |       -1 |     0 |    +2 |         +2 |
| Leichte Armbrust    | double |   -2 |       -3 |    -3 |    -3 |         -3 |
| Glefe               | double |   -2 |       +2 |    +2 |    +2 |         +2 |
| Großaxt             | double |   -3 |       -2 |    -1 |    +2 |         +3 |
| Großschwert         | double |   -2 |       +2 |    +3 |    +3 |         +2 |
| Hellebarde          | double |   -3 |       +1 |    +2 |    +2 |         +3 |
| Streithammer (Maul) | double |   -3 |       -2 |     0 |    +3 |         +3 |
| Pike                | double |   -3 |       +3 |    +2 |    +1 |         +1 |
| Schwere Armbrust    | double |   -3 |       -3 |    -3 |    -3 |         -3 |
| Langbogen           | double |    0 |       -3 |    -3 |    -3 |         -3 |

| Waffe               | Angriff   | Radiant |  Length | Speed               |
| ------------------- | --------- | ------: | -----: | ------------------- |
| Keule               | Hieb      |    100° |  80 cm | normal              |
| Dolch               | Stich     |     10° |  20 cm | fast                |
| Dolch               | Hieb      |     80° |  20 cm | fast                |
| Handaxt             | Hieb      |    100° |  40 cm | normal              |
| Wurfspeer           | Wurf      |      5° | 180 cm | normal              |
| Leichter Hammer     | Hieb      |    100° |  40 cm | normal              |
| Streitkolben        | Hieb      |    100° |  70 cm | normal              |
| Sichel              | Hieb      |    110° |  45 cm | fast                |
| Wurfpfeil           | Wurf      |      3° |  15 cm | fast                |
| Schleuder           | Projektil |      2° |      – | fast                |
| Dreschflegel        | Hieb      |    130° |  90 cm | normal              |
| Morgenstern         | Hieb      |    120° |  80 cm | normal              |
| Rapier              | Stich     |      8° | 110 cm | fast                |
| Rapier              | Hieb      |     60° | 110 cm | fast                |
| Krummsäbel          | Hieb      |    120° |  95 cm | fast                |
| Kurzschwert         | Stich     |     10° |  70 cm | fast                |
| Kurzschwert         | Hieb      |    100° |  70 cm | normal              |
| Kriegshacke         | Hieb      |     95° |  75 cm | normal              |
| Peitsche            | Schnalzen |     40° | 250 cm | normal                |
| Blasrohr            | Projektil |      2° | 150 cm | fast                |
| Handarmbrust        | Bolzen    |      2° |      – | fast                |
| Netz                | Wurf      |     - | - | langsames Projektil |
| Kampfstab (1H)      | Stoß      |     10° | 170 cm | normal              |
| Kampfstab (1H)      | Hieb      |    120° | 170 cm | normal              |
| Kampfstab (2H)      | Stoß      |     10° | 180 cm | normal              |
| Kampfstab (2H)      | Hieb      |    140° | 180 cm | normal              |
| Speer (1H)          | Stoß      |      8° | 230 cm | normal                |
| Speer (1H)          | Hieb      |     90° | 230 cm | normal              |
| Speer (2H)          | Stoß      |      8° | 260 cm | normal                |
| Speer (2H)          | Hieb      |    100° | 260 cm | normal              |
| Streitaxt (1H)      | Hieb      |    110° |  80 cm | normal              |
| Streitaxt (2H)      | Hieb      |    120° | 120 cm | normal              |
| Langschwert (1H)    | Stich     |      8° | 110 cm | normal                |
| Langschwert (1H)    | Hieb      |    110° | 110 cm | normal              |
| Langschwert (2H)    | Stich     |      8° | 120 cm | normal                |
| Langschwert (2H)    | Hieb      |    120° | 120 cm | normal              |
| Dreizack (1H)       | Stich     |     12° | 220 cm | normal                |
| Dreizack (2H)       | Stich     |     12° | 240 cm | normal                |
| Kriegshammer (1H)   | Hieb      |     90° |  75 cm | normal              |
| Kriegshammer (2H)   | Hieb      |    100° | 120 cm | normal              |
| Großer Knüppel      | Hieb      |    110° | 150 cm | normal              |
| Leichte Armbrust    | Bolzen    |      2° |      – | fast                |
| Glefe               | Hieb      |    130° | 220 cm | normal              |
| Glefe               | Stich     |     10° | 220 cm | fast                |
| Großaxt             | Hieb      |    130° | 160 cm | normal              |
| Großschwert         | Stich     |      8° | 170 cm | normal                |
| Großschwert         | Hieb      |    130° | 170 cm | normal              |
| Hellebarde          | Stich     |     10° | 240 cm | normal                |
| Hellebarde          | Hieb      |    130° | 240 cm | normal              |
| Streithammer (Maul) | Hieb      |    100° | 170 cm | normal              |
| Pike                | Stich     |      5° | 450 cm | normal                |
| Schwere Armbrust    | Bolzen    |      2° |      – | fast                |
| Langbogen           | Pfeil     |      2° |      – | fast                |

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