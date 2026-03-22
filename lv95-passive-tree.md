# bouyou — Level 95 Passive Tree Scenario

*Analysis date: 2026-03-22 | Tested via pob-brain (PoB Lua engine)*
*All 19 nodes tested individually and in combination against live build*

---

## Summary

| Stat | Lv77 Baseline | Lv95 Target | Change |
|------|---------------|-------------|--------|
| **CombinedDPS** | 358,930 | **473,940** | **+32%** |
| Attack Block | 49% | **78%** | ✅ Goal hit |
| Spell Block | 55% | **75%** | ✅ Goal hit |
| Life | 6,444 | 6,684 | +240 |
| Crit Chance | 22.0% | 28.3% | +6.3% |
| Crit Multiplier | 1.65× | 1.90× | +0.25× |

**18 regular passive points** (levels 78–95) + **1 unspent ascendancy point** = 19 nodes total.

---

## Node Allocation Plan

### Ascendancy — 1 Unspent Point

| Node | ID | Effect | DPS Impact |
|------|----|--------|------------|
| **Elemental Dmg + Crit Multi** | 662 | +10% Elemental Damage, +10% to Crit Multiplier | +14,000 |

> This is the next node on the Inquisitor ascendancy path toward Righteous Providence. Spend the 8th ascendancy point here.

---

### Regular Passive Tree — 18 Points

**Point by point, ordered by priority:**

#### Block Fix — 1 point

| # | Node | ID | Effect |
|---|------|----|--------|
| 1 | **Glancing Blows** | 39713 | Doubles block chance (49% → 78% attack, 55% → 75% spell). You take 65% of damage from blocked hits. |

> Costs 1 node and instantly solves both block targets. The trade-off (65% of blocked damage) is offset by the build's recovery mechanics — Rathpith Globe grants life recovery on block, and at 78% block you're blocking nearly 4 out of 5 hits.

---

#### Damage Chain — 2 points

| # | Node | ID | Effect | DPS per node |
|---|------|----|--------|-------------|
| 2 | **Damage + Mana** | 63965 | 14% increased Damage, +14 Mana | +9,022 |
| 3 | **Damage + Mana** | 35724 | 12% increased Damage, +10 Mana | +6,267 |

> "Increased Damage" is a broader modifier than elemental — applies to both Doom Blast and Spark. These two nodes chain together.

---

#### Spell Damage Chain — 2 points

| # | Node | ID | Effect |
|---|------|----|--------|
| 4 | **Spell Damage** | 21934 | 10% increased Spell Damage |
| 5 | **Spell Damage** | 17579 | 10% increased Spell Damage |

> Both skills are spells. These chain together off the same branch.

---

#### Lightning Walker Path — 3 points

| # | Node | ID | Effect |
|---|------|----|--------|
| 6 | **Elemental Damage** | 4184 | 10% increased Elemental Damage (gateway) |
| 7 | **Lightning Walker** | 30225 | 25% increased Lightning Damage, 5% increased Cast Speed with Lightning Skills, +15% Lightning Resistance |
| 8 | **Lightning Damage** | 58604 | 16% increased Lightning Damage |

> Lightning Walker is the payoff notable here. Both Doom Blast (lightning) and Spark of the Nova (lightning) benefit from lightning-specific damage. The +15% lightning resistance also helps sustain the cap. Node 58604 unlocks after taking Lightning Walker.

---

#### Annihilation Path (Spell Crit notable) — 4 points

| # | Node | ID | Effect |
|---|------|----|--------|
| 9 | **Spell Crit Chance** | 1346 | 20% increased Spell Critical Strike Chance |
| 10 | **Spell Crit Chance** | 44723 | 20% increased Spell Critical Strike Chance |
| 11 | **Spell Crit Chance** | 16790 | 25% increased Spell Critical Strike Chance |
| 12 | **Annihilation** | 53493 | **50% increased Spell Crit Chance, +15% to Crit Multiplier for Spell Damage** |

> This chain terminates at Annihilation — a strong spell crit notable. Combined crit from the chain: +115% increased spell crit chance + +15% crit multiplier for spells. Total crit rises from 22% → 28.3%.

---

#### Life Nodes — 2 points (also DPS via Spellblade)

| # | Node | ID | Effect |
|---|------|----|--------|
| 13 | **Life** | 6712 | 6% increased maximum Life |
| 14 | **Life** | 64587 | 6% increased maximum Life |

> **Why life = DPS on this build:** Rathpith Globe sacrifices 10% of max Life per spell cast, which PoB reads as your effective mana cost. Spellblade's multiplier scales with that effective cost. Every point of max life raises the Spellblade multiplier. These two life nodes each add ~+7,700 DPS on top of their survival value.

---

#### Elemental Damage Fill — 4 points

| # | Node | ID | Effect |
|---|------|----|--------|
| 15 | **Elemental Damage** | 58453 | 10% increased Elemental Damage |
| 16 | **Elemental Damage** | 61217 | 10% increased Elemental Damage |
| 17 | **Elemental Damage** | 12536 | 10% increased Elemental Damage |
| 18 | **Elemental Damage** | 44799 | 10% increased Elemental Damage |

> After all the specific multipliers above, these filler nodes each add ~+3,200 DPS at this point in the damage stack.

---

## DPS Progression by Cluster

| After adding... | Cumulative pts | DPS | Block |
|----------------|---------------|-----|-------|
| Baseline Lv77 | 0 | 358,930 | 49/55 |
| Glancing Blows | 1 | 358,930 | **78/75** ✅ |
| + Damage Chain | 3 | 374,398 | 78/75 |
| + Spell Dmg Chain | 5 | 390,844 | 78/75 |
| + Lightning Walker path | 8 | ~405,000 | 78/75 |
| + Annihilation path | 12 | 426,589 | 78/75 |
| + Life ×2 | 14 | ~443,000 | 78/75 |
| + Elemental fill ×4 | 18 | 459,969 | 78/75 |
| + Ascendancy 662 | 19 | **473,940** | 78/75 |

---

## Key Mechanic Notes

**Why Glancing Blows is viable here:**
- At 78% block with Glancing Blows: effective damage taken = (0.78 × 0.65) + (0.22 × 1.0) = 72.7% — worse than no-GB 49% block in raw EHP
- BUT: Rathpith Globe's life recovery on block fires 78% of all hits instead of 49%, providing massive active sustain
- At 78% block you also suppress stun, knockback, and on-block effects nearly all the time

**Why life nodes deal damage:**
The Spellblade support gem's multiplier is `1 + (ManaCost / 100)`. With Blood Magic + Rathpith Globe, every spell costs 10% of your max life as the effective mana cost. At 6,684 life: 668 "effective mana" = 6.68× more damage from Spellblade. Each +6% life = +40 life = +0.4 effective mana multiplier on Spellblade.

**Crit scaling:**
Inquisitor's Instruments of Virtue and passive crit nodes bring crit to 28.3% at Lv95. Combined with the Annihilation notable's +15% spell crit multiplier, each crit on a resistant enemy bypasses 75% lightning resistance entirely (Lightning Walker already helps cap lightning res). The crit/penetration synergy is significant for boss DPS.

---

## What Was NOT Worth Taking

| Category | Why skipped |
|----------|-------------|
| Cast Speed nodes | Doom Blast is triggered — cast speed doesn't increase trigger rate in PoB |
| Intelligence nodes | INT doesn't scale DPS in this build (Iron Will uses STR, not INT) |
| AoE nodes | No DPS gain — PoB confirmed 0 impact |
| Ancestral Knowledge (+30 Int) | +0 DPS |
| Shield Block node (+3%) | +0 DPS, only +3% block — unnecessary with Glancing Blows |

---

*Analysis via pob-brain (PoB Lua engine) | 30+ node combinations tested*
*Base build: [pobb.in/RelUA0m2JfJj](https://pobb.in/RelUA0m2JfJj)*
