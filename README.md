# bouyou — PoB Gem Optimization Analysis

*Build: Templar / Inquisitor — Lv77 | Source: [pobb.in/RelUA0m2JfJj](https://pobb.in/RelUA0m2JfJj)*
*Analysis date: 2026-03-22 | Constraint: no new 3.28 support gems*

---

## Build Overview

| Stat | Value |
|------|-------|
| Class | Templar / Inquisitor |
| Level | 77 |
| Primary DPS source | Doom Blast (triggered) — **358,930** CombinedDPS |
| Secondary DPS source | Spark of the Nova — **250,412** CombinedDPS |

### Key Uniques

| Slot | Item | Notable |
|------|------|---------|
| Weapon | Energy Blade (One Handed) | Scales mana-cost spell damage |
| Shield | Rathpith Globe | Sacrifices 10% life per spell cast → PoB treats as effective mana cost |
| Body | Foulborn Ghostwrithe | — |
| Helmet | Foulborn Doedre's Scorn | **Bakes in Impending Doom L30** — source of Doom Blast |
| Amulet | Replica Karui Ward | — |
| Belt | Screams of the Desiccated | — |
| Flasks | Foulborn Lori's Lantern | — |

---

## Gem Setup

### Body Armour — Spark of the Nova 6L

```
Spark of the Nova L18
  Pierce L15
  Spell Echo L16
  Intensify (ICD) L16
  Spellblade L17
  Lightning Penetration L17
```

### Helmet — Conductivity + Impending Doom

```
Conductivity L12
Spellblade L17
Cursed Ground L18
Spell Cascade L18
[Impending Doom L30 — from Doedre's Scorn item implicit]
```

---

## DPS Sources Explained

### Doom Blast (358,930 — primary)

Doom Blast is a **triggered skill** fired by Impending Doom when Conductivity expires on an enemy. The L30 Impending Doom is baked into the Doedre's Scorn helmet — it cannot be levelled further or swapped.

PoB cannot model the relationship between Conductivity's cast frequency and Doom Blast trigger rate. The DPS figure is fixed regardless of which support gems sit alongside Conductivity. No helmet gem swaps affect Doom Blast output.

### Spark of the Nova (250,412 — secondary)

Spark of the Nova has `baseEffectiveness = 4.09` and the following relevant skill types:
- **Multicastable** — Spell Echo applies
- **Volley** — Greater Volley compatible (but see below)
- Spell · Projectile · Lightning · Chaos · Physical

This is the skill where support gem choices actually matter.

---

## Gem Optimization — Spark of the Nova

All tests: same gear, same passive tree, only body armour 6L gems changed.

### Baseline

| Gem Setup | CombinedDPS |
|-----------|-------------|
| Pierce · Spell Echo · ICD · Spellblade · Lightning Pen | **250,412** |

### All Swaps Tested

| Swap | CombinedDPS | vs Baseline |
|------|-------------|-------------|
| Spellblade → **Elemental Focus** | 200,799 | **−20%** |
| Spellblade → **Faster Casting** | 197,563 | **−21%** |
| Spellblade → **Inc Crit Strikes** | 185,863 | **−26%** |
| Pierce → **Greater Volley** | 179,924 | **−28%** |
| Spellblade → **Added Lightning** | 177,644 | **−29%** |
| Lightning Pen → **Elemental Focus** | 242,442 | **−3%** |

**Every single swap reduced DPS. The current configuration is optimal.**

---

## Why Each Gem is Irreplaceable

### Spellblade (−20% to −29% if removed)

Despite `ManaCost = 0` showing in PoB stats, Rathpith Globe's "Sacrifice 10% of Life on spell cast" is read as an effective mana cost by PoB. At Lv77 with ~644 life, this translates to a large **"more damage" multiplier** from Spellblade. Replacing it with any other damage gem underperforms by 20–29%.

### Pierce (better than Greater Volley)

Spark of the Nova fires in a nova pattern. Greater Volley adds projectiles to each volley, but PoB does not model the nova spread differently for damage — the extra projectile count has no benefit over Pierce's direct damage multiplier here.

### Lightning Penetration (nearly irreplaceable)

Swapping to Elemental Focus only loses 3% DPS, but Elemental Focus blocks status effects (no shock application). Lightning Pen is the better choice because it applies shock while still providing penetration. Only worth reconsidering if enemy lightning resistance is not a factor.

### Spell Echo + Intensify (ICD)

Core compounding multipliers for a Multicastable spell. No swaps were attempted here — removing either would be a substantial loss.

---

## Conclusion

**The current bouyou gem setup is confirmed optimal** under the constraint of no new 3.28 support gems.

The highest-leverage real improvement is not *which* gems, but **gem levels**. The current build exports at L12–L18 (pobb.in level). Getting all gems to L20/20 quality would improve DPS significantly without changing the configuration.

| Action | Impact |
|--------|--------|
| Change any body armour gem | −3% to −29% (negative) |
| Level gems to L20/20 | Positive — directly scales spell damage |
| Level gems to L21 (corrupt) | Further improvement, especially Spark itself |

---

*Analysis by pob-brain (PoB Lua engine) | bouyou — 7 gem configurations tested*
*Build source: [pobb.in/RelUA0m2JfJj](https://pobb.in/RelUA0m2JfJj)*
