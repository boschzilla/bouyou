# Impending Doom — Meta Comparison & Mechanics Research (PoE 3.28 Mirage)

**100 builds scraped from poe.ninja · bouyou Lv95 Inquisitor comparison · Mechanics research from wiki + community guides**

---

## ⚠️ Critical Findings — Read First

### Doom Blast deals CHAOS damage. Not lightning.

This is the foundational fact that determines whether an Impending Doom build works.

| Assumption | Reality |
|---|---|
| Conductivity (-lightning res) buffs Doom Blast | ❌ Doom Blast is chaos. Lightning res reduction does nothing to it |
| Inevitable Judgement (crits ignore elemental res) helps ID damage | ❌ Elemental only. Chaos resistance is untouched |
| Inquisitor is a good class for Impending Doom | ❌ All of Inquisitor's kit is elemental/holy — zero chaos synergy |
| Spell Echo faster casts = bigger explosion | ❌ Doom stacking was removed in 3.20. Explosion is flat by gem level, 1s cooldown regardless |

---

## Impending Doom Mechanics (3.28)

### What Doom Blast actually is
- A **Chaos, Spell, AoE** hit triggered when a linked hex curse expires
- Triggers on a **1-second cooldown** per supported curse (affected by Cooldown Recovery Rate)
- Base damage at L20: **1,654–2,481 chaos**
- Base damage at L30 (via Doedre's Scorn helmet): roughly **double** the L20 value

### What scales Doom Blast

| Modifier | Scales? | Notes |
|---|---|---|
| Spell Damage | ✅ Yes | Explicitly confirmed |
| Chaos Damage | ✅ Yes | Core scaling axis |
| Gem Level | ✅ Yes | Steep scaling — L30 via Doedre's Scorn is a major upgrade |
| Curse Effect | ✅ Yes | Indirect scaling |
| Cooldown Recovery Rate (CDR) | ✅ Yes | More explosions per second |
| Effectiveness of Added Damage | ✅ 370% at L20 | Good for flat chaos added damage |
| Crit (base 5%) | ✅ Yes | Normal crit multiplier applies |
| Area Damage | ❓ Unconfirmed | AoE size scales with quality, but "area damage" mod likely does not apply |
| Lightning Damage / Conductivity | ❌ No | Doom Blast is chaos only |
| Elemental Penetration (Inevitable Judgement) | ❌ No | Chaos resistance is a separate stat |

### What does NOT scale it
- **Doom stacking (removed in 3.20)** — the old "1% increased curse effect per Doom, 60% more damage per 5 Doom" system is gone. Patch 3.20 doubled base damage to compensate.
- **Lightning resistance reduction (Conductivity)** — Doom Blast is not lightning damage
- **Elemental critical strike bonuses (Righteous Providence, Inevitable Judgement)** — all elemental, not chaos

### Curse choice comparison

| Curse | Effect on Doom Blast | Notes |
|---|---|---|
| **Despair** | ✅ Best | Reduces chaos res → directly multiplies Doom Blast damage |
| Temporal Chains | ✅ Good | Standard choice for the linked hex in most setups |
| Conductivity | ❌ Useless for damage | Reduces lightning res only. Used as filler/trigger placeholder in Vixen's Entrapment to force curse limit overflow — provides zero damage to Doom Blast |
| Vulnerability | ✅ Decent | Increases damage taken (physical + chaos builds) |

**Conductivity is a mechanical trigger tool in ID builds, not a damage modifier.**
It goes in the Vixen's Entrapment first socket (the one overwritten instantly) to force the curse limit so the real curse expires and detonates. Its debuff never applies for meaningful duration.

### Optimal 6L (no Doedre's Scorn)
```
Temporal Chains + Impending Doom Support + Spell Cascade + Unbound Ailments + Deadly Ailments + Cruelty
```

### With Doedre's Scorn (built-in L30 Impending Doom)
```
Temporal Chains + Spell Cascade + Awakened Unbound Ailments + Cruelty + Intensify + Awakened Deadly Ailments
```

### The Meta Setup (Occultist)
- **Class:** Occultist — Profane Bloom (chaos exposure), Malediction (extra curse), Void Beacon (chaos res reduction)
- **Helmet:** Doedre's Scorn — built-in L30 Impending Doom, massive base damage increase
- **Gloves:** Vixen's Entrapment — auto-triggers socketed curses on hex application
- **Linked hex:** Temporal Chains + Impending Doom Support
- **Second curse in gloves:** Despair (scales Doom Blast via chaos res reduction)
- **Filler curse in gloves:** Conductivity (trigger placeholder only)

---

## The bouyou Build Assessment

### What the build has

| Element | bouyou | ID-optimal |
|---|---|---|
| Class | Inquisitor | ❌ Occultist preferred |
| Curse | Conductivity | ❌ Despair or Temporal Chains |
| Ascendancy | Inevitable Judgement, Righteous Providence | ❌ Neither helps Doom Blast (chaos) |
| Helmet | Hubris Circlet (+1 Lightning Spells) | ❌ Doedre's Scorn for L30 ID |
| Gloves | Sorcerer Gloves (rare) | ❌ Vixen's Entrapment |
| Doom stacking assumption | Spell Echo = faster doom | ❌ Mechanic removed in 3.20 |

### Honest conclusion

The bouyou build is a **Lightning Inquisitor**. The gear (Rathpith Globe, Ghostwrithe, Pain Attunement low-life setup, Conductivity) is excellent for lightning spell damage. **Impending Doom does not synergize with any of it** because Doom Blast deals chaos, not lightning.

**Conductivity + Inevitable Judgement is actually a great combo** — but for lightning *hit* damage (Hexblast, Ball Lightning, Arc), not for Impending Doom explosions.

### Two paths forward

**Option A — Drop Impending Doom, return to a proper lightning skill**
Keep all the gear. Swap the 6L back to a lightning spell. Conductivity + Inevitable Judgement makes lightning hits penetrate all resistance after the shred — very strong, well-supported by the Inquisitor kit.

**Option B — Rebuild toward proper Impending Doom**
- Class → Occultist
- Helmet → Doedre's Scorn
- Gloves → Vixen's Entrapment
- Linked hex → Temporal Chains + Impending Doom Support
- Despair in gloves for chaos res reduction
- Conductivity as filler trigger only
- This is a fundamentally different build requiring significant gear changes.

---

## 100-Build Meta Analysis

### Ascendancy Distribution

| Ascendancy | Count | Notes |
|---|---|---|
| **Deadeye** | **27%** | Largest group — KB wand builds, not pure ID |
| Chieftain | 9% | Fire variant |
| Ascendant | 9% | Multi-class hybrid |
| Slayer | 9% | |
| Hierophant | 8% | |
| Pathfinder | 6% | |
| Champion | 6% | |
| Necromancer | 5% | |
| **Inquisitor** | **4%** | bouyou's class — least synergy with Doom Blast |
| Elementalist | 4% | |
| Gladiator | 3% | |
| Juggernaut | 3% | |
| Occultist | 3% | Meta ID class — underrepresented in this ladder scrape |
| Assassin | 2% | |
| Others | 3% | |

> Deadeye 27% are primarily Kinetic Blast wand builds — a different archetype that appears on poe.ninja's "Impending Doom" page due to secondary curse use.

### Key Uniques (100 builds)

| Item | % | Relevance |
|---|---|---|
| Watcher's Eye | 53% | Powerful for any build |
| Forbidden Flesh + Flame | 48% | Extra ascendancy node |
| Maloney's Mechanism | 43% | Bow trigger quiver (Deadeye builds only) |
| Lethal Pride | 40% | Keystone conversion |
| Thread of Hope | 33% | Cross-tree passive pathing |
| The Light of Meaning | 29% | General chaos/crit passive amplifier — no specific ID synergy |
| Mageblood | 27% | Flask automation |
| Headhunter | 25% | Mapping luxury |

### Curse Choice Across 100 Builds

| Curse | Count |
|---|---|
| Vulnerability | 10 |
| Despair | 9 |
| Punishment | 7 |
| Conductivity | 6 |
| Temporal Chains | 5 |

Conductivity appearing 6 times is consistent with it being used as a trigger placeholder, not a damage modifier.

### Keystones Across 100 Builds

| Keystone | Count |
|---|---|
| Mind Over Matter | 4 |
| Blood Magic | 4 |
| Pain Attunement | 2 |
| **Glancing Blows** | **1** |

Only 1/100 builds use Glancing Blows. Not recommended.

---

## Sources
- [Impending Doom Support — PoE Wiki](https://www.poewiki.net/wiki/Impending_Doom_Support)
- [Impending Doom Occultist Build Guide — Maxroll.gg](https://maxroll.gg/poe/build-guides/impending-doom-occultist/build-info-playstyle)
- [Inevitable Judgement — PoE Wiki](https://www.poewiki.net/wiki/Inevitable_Judgement)
- [Doedre's Scorn — PoE Wiki](https://www.poewiki.net/wiki/Doedre%27s_Scorn)
- [Vixen's Entrapment — PoE Wiki](https://www.poewiki.net/wiki/Vixen%27s_Entrapment)
- [PoE Doom Mechanic Explained — vhpg.com](http://www.vhpg.com/poe-doom/)
- 100 builds scraped from poe.ninja 3.28 Mirage ladder · 2026-03-22
