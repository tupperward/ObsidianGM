---
cssclasses:
  - hero-record
layout: Hero Record
name: ""
type: Humanlike
ancestry: ""
hero_class: ""
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
trained_melee: false
trained_ranged: false
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
---

# `= this.name`
*`= this.ancestry` · `= this.hero_class` · Level `= this.level`*
---
**HP** 0/`= this.hp_max` · **Armor** `= this.armor` · **Speed** `= this.speed` · **Fatigue** 0 · **Luck** 0/`= this.luck`

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
## Weapons

## Traits

## Abilities

## Magic

## Inventory
