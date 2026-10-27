# 5 Ottoman Sultans

An Unciv **extension mod** adding five playable Ottoman civilizations, each led by a different sultan and built around a different victory condition. Drop it in alongside the standard ruleset — it does not replace anything in the base game.

Each sultan gets a unique ability, a unique unit, a unique building and an AI personality tuned to their playstyle.

| Sultan | Victory focus | Unique ability | Unique unit | Unique building |
|---|---|---|---|---|
| Selim I | Domination | Conquests of Eight Years | Timarli Sipahi *(Knight)* | Cebhane-i Hümayun *(Armory)* |
| Mehmed II | Scientific | Sahn-ı Seman | Şahi Cannon *(Cannon)* | Tophane-i Amire *(Workshop)* |
| Suleiman I | Cultural | Magnificent Century | Mehteran *(Great General)* | Hasbahçe *(Garden)* |
| Selim III | Diplomatic | Permanent Embassies | Hariciye Envoy *(Great Merchant)* | Mühendishane-i Berrî *(University)* |
| Bayezid II | Cultural / Faith | Judicial Tolerance | Veli *(Missionary)* | Bayezid Külliyesi *(Temple)* |

## Installation

Unciv → **Mods** → **Download mod from URL**, paste this repository's URL. Or clone it into your Unciv `mods/` folder.

Enable it from the mod list when starting a game; the five sultans then appear in the civilization picker alongside the base-game nations.

Built against the current Unciv ruleset (verified on **4.22.x**). The `[This Unit] gets a name from the [...] group` unique requires **4.18.13 or newer**.

---

## The Sultans

### Selim I — Domination
*Conquests of Eight Years*
- `[+1] Movement <for [Land] units>`
- `[+15]% Production when constructing [Military] units [in all cities]`
- `[-25]% maintenance costs <for [Military] units>`
- `Earn [50]% of killed [Military] unit's [Strength] as [Gold]`

### Mehmed II — Scientific
*Sahn-ı Seman*
- `[+1 Science] per [3] population [in all cities]`
- `[Great Scientist] is earned [25]% faster`
- `[Great Engineer] is earned [25]% faster`
- `[+25]% Production when constructing [Siege] units [in all cities]`

### Suleiman I — Cultural
*Magnificent Century*
- `[+50]% Golden Age length`
- `[+25]% Great Person generation [in all cities]`
- `[Great Artist] is earned [25]% faster`
- `[+30]% [Culture] <during a Golden Age>`
- `Earn [50]% of killed [Military] unit's [Strength] as [Culture]`

### Selim III — Diplomatic
*Permanent Embassies*
- `Resting point for Influence with City-States is increased by [10]`
- `[-50]% City-State Influence degradation`
- `Gifts of Gold to City-States generate [25]% more Influence`
- `Allied City-States provide [Science] equal to [25]% of what they produce for themselves`

### Bayezid II — Cultural / Faith
*Judicial Tolerance*
- `[+25]% [Faith]`
- `[+1 Happiness] [in all cities] <in cities following our religion>`
- `[-25]% Faith cost of generating Great Prophet equivalents`
- `[+25]% Spread Religion Strength`

---

## Unique Units

Figures in brackets are the base unit's value, for comparison.

### Timarli Sipahi — replaces Knight *(Selim I)*
4 Movement, 20 Strength, 120 Production, requires Horses.
- `Ignores terrain cost` — **new**
- `No movement cost to pillage` — **new**
- Plus the Knight's own `Can move after attacking`, `No defensive terrain bonus` and `[-33]% Strength <vs cities> <when attacking>`.

### Şahi Cannon — replaces Cannon *(Mehmed II)*
2 Movement, 14 Strength, **26** Ranged Strength *(20)*, Range 2, 185 Production.
- Keeps the Cannon's `[+200]% Strength <vs cities> <when attacking>` and `Must set up to ranged attack`.
- The buff is raw ranged power; range and mobility match the Cannon.

### Mehteran — replaces Great General *(Suleiman I)*
3 Movement *(2)*.
- `Empire enters a [8]-turn Golden Age <by consuming this unit>` — **new**, and Suleiman's `[+50]% Golden Age length` makes that 12 turns.
- Otherwise a full Great General: `[+15]% Strength bonus for [Military] units within [2] tiles`, Citadel construction, earned through combat.

### Hariciye Envoy — replaces Great Merchant *(Selim III)*
3 Movement *(2)*.
- Trade mission gives **50** Influence *(30)*.
- `[+100]% Gold from Great Merchant trade missions` — **new**.
- Otherwise a full Great Merchant: Customs house construction, shares the standard Great Person pool.

### Veli — replaces Missionary *(Bayezid II)*
5 Movement *(4)*.
- Spreads religion **3** times *(2)*.
- Loses only **150** religious strength per turn in foreign territory *(250)*.
- Faith-purchasable like any Missionary.

---

## Unique Buildings

### Cebhane-i Hümayun — replaces Armory *(Selim I)*
130 Production *(160)*, 1 Maintenance.
- `New [Military] units start with [20] XP [in this city]` *(15)*

### Tophane-i Amire — replaces Workshop *(Mehmed II)*
120 Production, 2 Maintenance. +2 Production, **+1 Science**, 1 Engineer slot.
- `[+15]% Production [in this city]` *(10%)*
- `[+30]% Production when constructing [Siege] units [in this city]` — **new**

### Hasbahçe — replaces Garden *(Suleiman I)*
120 Production, 1 Maintenance. **+3 Culture**.
- `[+25]% Great Person generation [in this city]`
- Drops the Garden's `Must be next to [Fresh water]` requirement — build it anywhere.

### Mühendishane-i Berrî-i Hümâyûn — replaces University *(Selim III)*
160 Production, 2 Maintenance. **+2 Science**, **+2 Culture**, 2 Scientist slots.
- `[+33]% [Science] [in this city]` and `[+2 Science] from [Jungle] tiles [in this city]`
- `New [Water] units start with [15] XP [in this city]` — **new** (coastal cities only)

### Bayezid Külliyesi — replaces Temple *(Bayezid II)*
100 Production, **1** Maintenance *(2)*. **+5 Faith** *(2)*, **+2 Food**, **+1 Culture**.

---

## A note on `replaces`

Unciv does **not** inherit stats or abilities from the building or unit being replaced. A replacement starts from nothing, so every stat and unique it should keep has to be written out again in full.

That means the numbers above are the *actual, final* values — there is no hidden base layer stacking underneath them. An earlier version of this README added base and custom figures together and overstated several buildings as a result.

## Credits

Nation, unit and building icons are AI-generated. Ruleset values are checked against the Civ V — Gods & Kings ruleset shipped with Unciv.
