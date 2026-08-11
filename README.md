# Unciv Modding Guide: 5 Ottoman Sultans Mod

This document is a comprehensive technical specification guide written in English for another AI (or developer) to generate the exact Unciv mod JSON files (`Nations.json`, `Units.json`, `Buildings.json`, `ModOptions.json`) and run automated test validations.

---

## 📂 1. Directory Structure
The mod folder structure following Unciv standards must be:

```text
OttomanSultansMod/
├── ModOptions.json
└── jsons/
    ├── Nations.json
    ├── Units.json
    └── Buildings.json
```

---

## ⚙️ 2. General Mod Settings (`ModOptions.json`)
```json
{
  "name": "OttomanSultansMod",
  "author": "Unciv Modder",
  "description": "5 Ottoman Sultans tailored for 5 Victory Conditions (Selim I, Mehmed II, Suleiman I, Selim III, Bayezid II)",
  "minVersion": "4.0.0"
}
```

---

## 👑 3. Civilizations & Leader Traits (`jsons/Nations.json`)

### ⚔️ 1. SELIM I (Domination Victory)
* **Nation Name:** `Ottoman Empire (Selim I)`
* **Leader Name:** `Selim I (The Grim)`
* **Unique Ability (UA) Name:** `Conquests of Eight Years`
* **UA Uniques:**
  - `"[+1] Movement <for [Military] units>"`
  - `"[-25]% Resistance length when capturing cities"`
  - `"[50]% less population lost when capturing cities"`
* **Unique Unit (UU):** `Timarli Sipahi` (replaces Knight)
* **Unique Building (UB):** `Cebhane-i Hümayun` (replaces Armory)

### 🧪 2. MEHMED II (Science Victory)
* **Nation Name:** `Ottoman Empire (Mehmed II)`
* **Leader Name:** `Mehmed II (The Conqueror)`
* **Unique Ability (UA) Name:** `Sahn-ı Seman`
* **UA Uniques:**
  - `"[+1 Science] per [3] population [in all cities]"`
  - `"[+30]% Great Person Generation <for [Great Scientist] units>"`
  - `"[+30]% Great Person Generation <for [Great Engineer] units>"`
* **Unique Unit (UU):** `Şahi Cannon` (replaces Cannon)
* **Unique Building (UB):** `Tophane-i Amire` (replaces Workshop)

### 🎨 3. SULEIMAN I (Culture Victory)
* **Nation Name:** `Ottoman Empire (Suleiman I)`
* **Leader Name:** `Suleiman I (The Magnificent)`
* **Unique Ability (UA) Name:** `Magnificent Century`
* **UA Uniques:**
  - `"[+50]% Golden Age length"`
  - `"[+30]% [Culture] <during a Golden Age>"`
  - `"[+1] Influence per turn with City-States <during a Golden Age>"`
* **Unique Unit (UU):** `Mehteran` (replaces Great General)
* **Unique Building (UB):** `Hasbahçe` (replaces Garden)

### 🕊️ 4. SELIM III (Diplomatic Victory)
* **Nation Name:** `Ottoman Empire (Selim III)`
* **Leader Name:** `Selim III`
* **Unique Ability (UA) Name:** `Permanent Embassies`
* **UA Uniques:**
  - `"Base Influence with City-States is [10]"`
  - `"[-50]% Influence decay with City-States"`
* **Unique Unit (UU):** `Hariciye Envoy` (replaces Great Merchant)
* **Unique Building (UB):** `Mühendishane-i Berrî-i Hümâyûn` (replaces University)

### 🕌 5. BAYEZID II (Religious Victory)
* **Nation Name:** `Ottoman Empire (Bayezid II)`
* **Leader Name:** `Bayezid II (The Just)`
* **Unique Ability (UA) Name:** `Judicial Tolerance`
* **UA Uniques:**
  - `"[+25]% [Faith]"`
  - `"[+1 Happiness] per city following your religion"`
* **Unique Unit (UU):** `Veli` (replaces Missionary)
* **Unique Building (UB):** `Bayezid Külliyesi` (replaces Temple)

---

## 🗡️ 4. Unique Units Configuration (`jsons/Units.json`)

1. **Timarli Sipahi**
   - **Replaces:** `Knight`
   - **Uniques:** 
     - `"Can move at full speed on rough terrain"`
     - `"Pillaging tiles costs no movement points"`

2. **Şahi Cannon**
   - **Replaces:** `Cannon`
   - **Stats:** `strength`: 12, `rangedStrength`: 26, `movement`: 1, `range`: 3
   - **Uniques:** `"[+200]% Strength <vs cities>", "Must set up to ranged attack"`

3. **Mehteran**
   - **Replaces:** `Great General`
   - **Uniques:**
     - `"[+15]% Strength <for [Military] units> <in tiles adjacent to this unit>"`
     - `"Earn [50]% of killed unit's [Strength] as [Culture]"`

4. **Hariciye Envoy**
   - **Replaces:** `Great Merchant`
   - **Uniques:**
     - `"Gains extra gold and influence when conducting a trade mission"`
     - `"Can undertake a trade mission in City-State territory"`

5. **Veli**
   - **Replaces:** `Missionary`
   - **Stats:** `movement`: 5, `religionSpreads`: 3
   - **Uniques:** `"Can spread religion"`

---

## 🏛️ 5. Unique Buildings Configuration (`jsons/Buildings.json`)

1. **Cebhane-i Hümayun** (Selim I)
   - **Replaces:** `Armory`
   - **Uniques:** `"[+15] XP for [Military] units"`, `"[-15]% maintenance costs for [Military] units"`

2. **Tophane-i Amire** (Mehmed II)
   - **Replaces:** `Workshop`
   - **Uniques:** `"[+30]% Production when constructing [{Siege}] units"`, `"[+1 Science]"`, `"[+2 Production]"`

3. **Hasbahçe** (Suleiman I)
   - **Replaces:** `Garden` (No fresh water requirement)
   - **Uniques:** `"[+3 Culture]"`, `"[+25]% Great Person Generation in this city"`

4. **Mühendishane-i Berrî-i Hümâyûn** (Selim III)
   - **Replaces:** `University`
   - **Uniques:**
     - `"[+2 Culture]"`
     - `"[+15] XP for [{Water}] units"`
     - `"[+33]% [Science] [in this city]"`
     - `"[+2 Science]"`

5. **Bayezid Külliyesi** (Bayezid II)
   - **Replaces:** `Temple`
   - **Uniques:**
     - `"[+5 Faith]"`
     - `"[+2 Food]"`
     - `"[+1 Culture]"`

---

## 🧪 6. AI Testing & Validation Protocol

The code-generating AI (or developer) MUST validate the mod through the following 3-step process after generating the JSON files:

### Step 1: JSON Syntax & Parsing Validation
1. Verify that all generated `.json` files are valid JSON objects using a JSON linter or `JSON.parse()`.
2. Ensure there are no unclosed brackets `[`, braces `{`, or missing quotes.

### Step 2: Unciv Built-in Ruleset Validator
Unciv features a built-in syntax and object reference checker.
1. Place the mod directory into the Unciv `mods/` directory and launch the game.
2. Navigate to **Options -> Locate Mod Errors (Ruleset Validator)**.
3. Verify there are zero errors logged (ensure all referenced base objects like `Cannon`, `University`, `Knight`, `Great General`, `Great Merchant`, `Missionary`, `Armory`, `Workshop`, `Garden`, `Temple` exist in the ruleset).

### Step 3: Automated AI Autoplay & Spectator Simulation
To verify the mod does not cause game-breaking crashes or NullPointerExceptions:
1. In the Game Setup screen (Singleplayer -> Custom Game):
   - Add all 5 Ottoman leaders from this mod to the 5 player slots (Selim I, Mehmed II, Suleiman I, Selim III, Bayezid II).
   - Enable "Spectator / Autoplay" mode and set turn speed to maximum.
2. Simulate at least 100 turns automatically.
3. Confirm that buildings can be constructed, units can be trained, and unique abilities execute without crashing the game engine.
