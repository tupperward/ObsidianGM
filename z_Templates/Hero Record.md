---
cssclasses:
  - hero-record
layout: Hero Record
name: ""
type: Humanlike
ancestry: ""
class: ""
level: 1
xp: 0
might: 2
dexterity: 2
awareness: 2
reason: 2
presence: 2
luck: 2
hp: 0
hp_max: 0
armor: 0
speed: 25'
fatigue: 0
current_luck: 2
mana: 0
mana_max: 0
casting_max: 0
trained_arcana: false
trained_brawl: false
trained_craft: false
trained_detect: false
trained_finesse: false
trained_influence: false
trained_leadership: false
trained_medicine: false
trained_mysticism: false
trained_performance: false
trained_sneak: false
trained_survival: false
weapon1_name: ""
weapon1_traits: ""
weapon2_name: ""
weapon2_traits: ""
weapon3_name: ""
weapon3_traits: ""
abilities: ""
spells: ""
wealth: 0G 0S 0C
item_slots: 10
inv1: ""
inv1_slots: 0
inv2: ""
inv2_slots: 0
inv3: ""
inv3_slots: 0
inv4: ""
inv4_slots: 0
inv5: ""
inv5_slots: 0
inv6: ""
inv6_slots: 0
inv7: ""
inv7_slots: 0
inv8: ""
inv8_slots: 0
inv9: ""
inv9_slots: 0
inv10: ""
inv10_slots: 0
---
# `VIEW[{name}][text]`
*`VIEW[{ancestry}][text]` · `VIEW[{class}][text]` · Level `VIEW[{level}][text]`*
---
## Identity
|           |                     |              |                        |
| --------- | ------------------- | ------------ | ---------------------- |
| **Name**  | `INPUT[text:name]`  | **Ancestry** | `INPUT[text:ancestry]` |
| **Class** | `INPUT[text:class]` | **Level**    | `INPUT[number:level]`  |
| **Type**  | `INPUT[text:type]`  | **XP**       | `INPUT[number:xp]`     |
---
## Stats
|          MIT          |            DEX            |            AWR            |          RSN           |           PRS            |         LCK          |
| :-------------------: | :-----------------------: | :-----------------------: | :--------------------: | :----------------------: | :------------------: |
| `INPUT[number:might]` | `INPUT[number:dexterity]` | `INPUT[number:awareness]` | `INPUT[number:reason]` | `INPUT[number:presence]` | `INPUT[number:luck]` |
---
## Combat
| | | | |
|---|---|---|---|
| **HP** | `INPUT[number:hp]` / `INPUT[number:hp_max]` | **Armor** | `INPUT[number:armor]` |
| **Speed** | `INPUT[text:speed]` | **Fatigue** | `INPUT[number:fatigue]` |
| **Current Luck** | `INPUT[number:current_luck]` | | |
---
## Saves
| Reflex | Endure | Will |
|:---:|:---:|:---:|
| `VIEW[20 - {dexterity} - {awareness}][math]` | `VIEW[20 - {might} - {might}][math]` | `VIEW[20 - {reason} - {presence}][math]` |
---
## Skills
| Skill | T | Target | Skill | T | Target |
|---|:---:|:---:|---|:---:|:---:|
| **Arcana** | `INPUT[toggle:trained_arcana]` | `VIEW[20 - {reason} * (1 + number({trained_arcana}))][math]` | **Leadership** | `INPUT[toggle:trained_leadership]` | `VIEW[20 - {presence} * (1 + number({trained_leadership}))][math]` |
| **Brawl** | `INPUT[toggle:trained_brawl]` | `VIEW[20 - {might} * (1 + number({trained_brawl}))][math]` | **Medicine** | `INPUT[toggle:trained_medicine]` | `VIEW[20 - {reason} * (1 + number({trained_medicine}))][math]` |
| **Craft** | `INPUT[toggle:trained_craft]` | `VIEW[20 - {reason} * (1 + number({trained_craft}))][math]` | **Mysticism** | `INPUT[toggle:trained_mysticism]` | `VIEW[20 - {awareness} * (1 + number({trained_mysticism}))][math]` |
| **Detect** | `INPUT[toggle:trained_detect]` | `VIEW[20 - {awareness} * (1 + number({trained_detect}))][math]` | **Performance** | `INPUT[toggle:trained_performance]` | `VIEW[20 - {presence} * (1 + number({trained_performance}))][math]` |
| **Finesse** | `INPUT[toggle:trained_finesse]` | `VIEW[20 - {dexterity} * (1 + number({trained_finesse}))][math]` | **Sneak** | `INPUT[toggle:trained_sneak]` | `VIEW[20 - {dexterity} * (1 + number({trained_sneak}))][math]` |
| **Influence** | `INPUT[toggle:trained_influence]` | `VIEW[20 - {presence} * (1 + number({trained_influence}))][math]` | **Survival** | `INPUT[toggle:trained_survival]` | `VIEW[20 - {awareness} * (1 + number({trained_survival}))][math]` |
---
## Rolls
| Hindered | Check | Favored |
|:---:|:---:|:---:|
| `dice: hindered` | `dice: check` | `dice: favored` |
---
## Attacks
| Melee | Ranged | Brawl | Finesse |
|:---:|:---:|:---:|:---:|
| `VIEW[20 - {might}][math]` | `VIEW[20 - {awareness}][math]` | `VIEW[20 - {might} * (1 + number({trained_brawl}))][math]` | `VIEW[20 - {dexterity} * (1 + number({trained_finesse}))][math]` |
---
## Weapons
| Weapon                     | Damage      | Traits                       |
| -------------------------- | ----------- | ---------------------------- |
| `INPUT[text:weapon1_name]` | `dice: 1d4` | `INPUT[text:weapon1_traits]` |
| `INPUT[text:weapon2_name]` | `dice: 1d6` | `INPUT[text:weapon2_traits]` |
| `INPUT[text:weapon3_name]` | `dice: 1d8` | `INPUT[text:weapon3_traits]` |
| `INPUT[text:weapon3_name]` |  | `INPUT[text:weapon3_traits]` |
---
## Abilities
`INPUT[textArea:abilities]`
---
## Magic
| | | | |
|---|---|---|---|
| **Mana** | `INPUT[number:mana]` / `INPUT[number:mana_max]` | **Casting Max** | `INPUT[number:casting_max]` |
`INPUT[textArea:spells]`
---
## Inventory
| | | | |
|---|---|---|---|
| **Wealth** | `INPUT[text:wealth]` | **Slots** | `VIEW[{inv1_slots} + {inv2_slots} + {inv3_slots} + {inv4_slots} + {inv5_slots} + {inv6_slots} + {inv7_slots} + {inv8_slots} + {inv9_slots} + {inv10_slots}][math]` / `INPUT[number:item_slots]` |
| # | Item | Slots |
|:---:|---|:---:|
| 1 | `INPUT[text:inv1]` | `INPUT[number:inv1_slots]` |
| 2 | `INPUT[text:inv2]` | `INPUT[number:inv2_slots]` |
| 3 | `INPUT[text:inv3]` | `INPUT[number:inv3_slots]` |
| 4 | `INPUT[text:inv4]` | `INPUT[number:inv4_slots]` |
| 5 | `INPUT[text:inv5]` | `INPUT[number:inv5_slots]` |
| 6 | `INPUT[text:inv6]` | `INPUT[number:inv6_slots]` |
| 7 | `INPUT[text:inv7]` | `INPUT[number:inv7_slots]` |
| 8 | `INPUT[text:inv8]` | `INPUT[number:inv8_slots]` |
| 9 | `INPUT[text:inv9]` | `INPUT[number:inv9_slots]` |
| 10 | `INPUT[text:inv10]` | `INPUT[number:inv10_slots]` |
