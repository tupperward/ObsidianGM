---
cssclasses:
  - hero-record
layout: Hero Record
name: Llewyn Davis
type: Humanlike
ancestry: "[[Elf]]"
hero_class: "[[Gunslinger]]"
level: 1
xp: 0
might: 4
dexterity: 4
awareness: 7
reason: 4
presence: 4
luck: 2
hp: 0
hp_max: 3
armor: 1
speed: 35'
fatigue: 0
current_luck: 4
trained_melee: false
trained_ranged: true
trained_arcana: false
trained_brawl: true
trained_craft: false
trained_detect: true
trained_finesse: false
trained_influence: false
trained_leadership: false
trained_medicine: false
trained_mysticism: true
trained_performance: false
trained_sneak: true
trained_survival: true
---
# `= this.name`
*`= this.ancestry` · `= this.hero_class` · Level `= this.level`*
---
**HP** 3/`= this.hp_max` · **[[Armor]]** `= this.armor` · **Speed** `= this.speed` · **Fatigue** 0 · **Luck** 2/`= this.luck`

| MIT | DEX | AWR | RSN | PRS | LCK |
|:---:|:---:|:---:|:---:|:---:|:---:|
| `= this.might` | `= this.dexterity` | `= this.awareness` | `= this.reason` | `= this.presence` | `= this.luck` |

| Reflex | Endure | Will | Hindered | Check | Favored |
|:---:|:---:|:---:|:---:|:---:|:---:|
| `= 20 - this.dexterity - this.awareness` | `= 20 - this.might * 2` | `= 20 - this.reason - this.presence` | `dice: hindered` | `dice: check` | `dice: favored` |

| Skill | Target | Skill | Target |
|---|:---:|---|:---:|
| **[[Arcana]]** | `= choice(this.trained_arcana, 20 - this.reason * 2, 20 - this.reason)` | **[[Leadership]]** | `= choice(this.trained_leadership, 20 - this.presence * 2, 20 - this.presence)` |
| **[[Brawl]]** | `= choice(this.trained_brawl, 20 - this.might * 2, 20 - this.might)` | **[[Medicine]]** | `= choice(this.trained_medicine, 20 - this.reason * 2, 20 - this.reason)` |
| **[[Craft]]** | `= choice(this.trained_craft, 20 - this.reason * 2, 20 - this.reason)` | **[[Mysticism]]** | `= choice(this.trained_mysticism, 20 - this.awareness * 2, 20 - this.awareness)` |
| **[[Detect]]** | `= choice(this.trained_detect, 20 - this.awareness * 2, 20 - this.awareness)` | **[[Performance]]** | `= choice(this.trained_performance, 20 - this.presence * 2, 20 - this.presence)` |
| **[[Finesse]]** | `= choice(this.trained_finesse, 20 - this.dexterity * 2, 20 - this.dexterity)` | **[[Sneak]]** | `= choice(this.trained_sneak, 20 - this.dexterity * 2, 20 - this.dexterity)` |
| **[[Influence]]** | `= choice(this.trained_influence, 20 - this.presence * 2, 20 - this.presence)` | **[[Survival]]** | `= choice(this.trained_survival, 20 - this.awareness * 2, 20 - this.awareness)` |

| Melee | Ranged | Brawl | Finesse |
|:---:|:---:|:---:|:---:|
| `= choice(this.trained_melee, 20 - this.might * 2, 20 - this.might)` | `= choice(this.trained_ranged, 20 - this.awareness * 2, 20 - this.awareness)` | `= choice(this.trained_brawl, 20 - this.might * 2, 20 - this.might)` | `= choice(this.trained_finesse, 20 - this.dexterity * 2, 20 - this.dexterity)` |

---
## Attacks

| Weapon  | Grip | Damage                             | Properties   | Range |
| ------- | ---- | ---------------------------------- | ------------ | ----- |
| Rifle   | 2H   | `dice: 1d8` / Marksman: `dice: 1d10` | Keen, Ranged | Far   |
| Handgun | 1H   | `dice: 1d4` / Marksman: `dice: 1d6`      | Ranged       | Far   |

---
## Perks
- [[Marksmanship]]
---
## Traits
- [[Elven Eyes]]
- [[Naturally Attuned]]
---
## Abilities
- [[Quick Draw]]
- [[Deadeye]] `dice: 1d20`
---
## Magic
- [[Dispel]]
---
## Inventory
Max Slots: `=this.might + 8`

| Item            | Slots |
| --------------- | ----- |
| Rifle           | 2     |
| Handgun         | 1     |
| Box of Bullets  | 1     |
| Rope            | 1     |
| Manacles        | 1     |
| Lockpicks (3)   | 1     |
| L. Armor        | 2     |
| **Total Slots** | 9     |
<!-- TBLFM: @>$2=sum(@I..@-1) -->


