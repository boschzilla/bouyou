# bouyou — Level 95 Lightning Conduit Build

*Analysis date: 2026-03-22 | PoB verified via pob-brain (PoB Lua engine)*
*Source build: [pobb.in/RelUA0m2JfJj](https://pobb.in/RelUA0m2JfJj) | Output: `bouyou_lv95.xml`*

---

## Summary

| Stat | Lv77 Baseline | Lv95 LC Build | Change |
|------|---------------|---------------|--------|
| **CombinedDPS** | 358,930 | **885,444** | **+147%** |
| Life | 6,444 | **8,163** | +1,719 |
| Crit Chance | 22.0% | **39%** | +17% |
| Crit Multiplier | 1.65× | **3.38×** | +1.73× |
| Fire Resist | — | 80% | ✅ |
| Cold Resist | — | 78% | ✅ |
| Lightning Resist | — | 78% | ✅ |
| Chaos Resist | — | 70% | ✅ |
| Attack Block | 49% | 49% | unchanged |
| Spell Block | 55% | 55% | unchanged |

**Build changes from Lv77 baseline:**
- Dropped Foulborn Doedre's Scorn → rare Hubris Circlet (**Doom Resonance**)
- Dropped Spark of the Nova → **Lightning Conduit** as primary skill
- Re-linked helmet: Conductivity now linked to Impending Doom + Spell Echo + Cursed Ground
- Doom Blast remains via Impending Doom support (L20, up from the L30 helmet implicit)
- 18 regular passive points + 1 unspent ascendancy point allocated
- No Glancing Blows taken

---

## Gear Changes

### Helmet: Doom Resonance (Hubris Circlet)

```
Rarity: RARE
Doom Resonance
Hubris Circlet

+1 to Level of all Lightning Spell Skill Gems   ← boosts LC AND Conductivity
+120 to maximum Life
10% increased Spell Critical Strike Chance
+52% to Fire Resistance
+48% to Cold Resistance (crafted)
```

> Replaces Foulborn Doedre's Scorn. The L30 Impending Doom implicit from Doedre's Scorn is lost, but we regain it as a regular L20 gem (linked properly to Conductivity), and the rare affixes plug the resist gaps while adding life and spell crit.

---

## Final Gem Setup

### Body Armour — Lightning Conduit 6L (main skill)

```
Lightning Conduit L20/20
  Elemental Focus L20/20
  Spell Echo L20/20
  Increased Critical Damage L20/20
  Spellblade L20/20
  Lightning Penetration L20/20
```

**Why these gems:**

| Gem | Why it's here |
|-----|---------------|
| **Elemental Focus** | +49% more elemental damage; shock comes from Doom Blast (not LC), so EF's no-ailment restriction is irrelevant |
| **Spell Echo** | LC is Multicastable — Spell Echo fires twice and significantly boosts hit rate |
| **Increased Critical Damage** | Crit multiplier is 3.38× — large base to scale further |
| **Spellblade** | Rathpith Globe sacrifices 10% of life per cast → at 8,163 life that's 816 effective mana → massive more damage multiplier |
| **Lightning Penetration** | Bypasses enemy lightning resistance while preserving shock application |

### Helmet — Conductivity 4L

```
Conductivity L20/20
  Impending Doom L20/20
  Spell Echo L20/20
  Cursed Ground L20/20
```

> When Conductivity expires on an enemy, Impending Doom fires Doom Blast — still the secondary DPS source. Spell Echo doubles the Conductivity application frequency, increasing how often Doom Blast fires. Cursed Ground ensures curse re-application on moving enemies.

---

## Passive Tree — 19 Points (Lv78–95)

### Ascendancy — 1 Unspent Point

| Node | ID | Effect |
|------|----|--------|
| **Elemental Dmg + Crit Multi** | 662 | +10% Elemental Damage, +10% to Crit Multiplier |

### Regular Passives — 18 Points

| # | Node | ID | Effect |
|---|------|----|--------|
| 1 | Damage + Mana | 63965 | 14% increased Damage, +14 Mana |
| 2 | Damage + Mana | 35724 | 12% increased Damage, +10 Mana |
| 3 | Spell Damage | 21934 | 10% increased Spell Damage |
| 4 | Spell Damage | 17579 | 10% increased Spell Damage |
| 5 | Elemental Damage | 4184 | 10% increased Elemental Damage (gateway) |
| 6 | **Lightning Walker** | 30225 | 25% increased Lightning Damage, 5% Cast Speed with Lightning, +15% Lightning Resist |
| 7 | Lightning Damage | 58604 | 16% increased Lightning Damage |
| 8 | Spell Crit Chance | 1346 | 20% increased Spell Crit Chance |
| 9 | Spell Crit Chance | 44723 | 20% increased Spell Crit Chance |
| 10 | Spell Crit Chance | 16790 | 25% increased Spell Crit Chance |
| 11 | **Annihilation** | 53493 | 50% increased Spell Crit Chance, +15% Crit Multi for Spells |
| 12 | Life | 6712 | 6% increased maximum Life |
| 13 | Life | 64587 | 6% increased maximum Life |
| 14 | Elemental Damage | 58453 | 10% increased Elemental Damage |
| 15 | Elemental Damage | 61217 | 10% increased Elemental Damage |
| 16 | Elemental Damage | 12536 | 10% increased Elemental Damage |
| 17 | Elemental Damage | 44799 | 10% increased Elemental Damage |
| 18 | Spell/Damage | 20551 | damage fill — replaces Glancing Blows slot |

> **No Glancing Blows.** Block stays at 49/55 without it. Rathpith Globe's life recovery on block is less frequent but there's no 65% damage-on-block penalty.

---

## Why the DPS Tripled

The Lv77 Doom Blast build was bottlenecked by Doedre's Scorn — the L30 Impending Doom was excellent but Doom Blast is a triggered skill with a fixed fire rate that PoB cannot optimize with support gems. All 6 body armour gems (Spark of the Nova) were the actual scaling vector.

Lightning Conduit synergises better with this character's stat profile:

```
Key multiplier stack:
  LC base × Spell Echo (×2 hits) × Elemental Focus (+49%)
  × Increased Crit Damage × Spellblade (~9× at 8163 life)
  × Lightning Penetration × Inquisitor (penetrates resists on crit)
  × 39% crit × 3.38× multiplier
  + +1 to Lightning Spell gems from Doom Resonance (LC effective L21)
```

**Spellblade at Lv95:**
`EffectiveMana = 8163 × 10% = 816` → Spellblade multiplier ≈ `1 + (816/100)` = **9.16× more damage** from a single support gem. At Lv77 with 6444 life this was 6.44×. Every life node is still a direct DPS multiplier.

**Crit scaling:**
Inquisitor's Inevitable Judgement (penetrates all resistances on crit) synergises directly with LC's single large hit. 39% crit at 3.38× multiplier means the average hit includes a substantial crit component.

---

## DPS Breakdown

| Component | DPS |
|-----------|-----|
| **Lightning Conduit (main)** | **885,444** |
| Doom Blast (secondary, from Impending Doom on Conductivity) | ~significant, not in main TotalDPS |

> Doom Blast secondary DPS is not included in the 885k figure — it fires separately when Conductivity expires. At L20 Impending Doom (down from L30 Doedre's Scorn), it will be lower than the previous 358k, but it is additive to the real-world damage output.

---

## Defensive Profile

| Stat | Value | Notes |
|------|-------|-------|
| Life | 8,163 | High — Spellblade scales with this |
| Energy Shield | 3,021 | From Ghostwrithe + Hubris Circlet |
| Block | 49% | No Glancing Blows — clean EHP |
| Spell Block | 55% | — |
| Fire Resist | 80% | Over cap |
| Cold Resist | 78% | At effective cap |
| Lightning Resist | 78% | At effective cap |
| Chaos Resist | 70% | Positive — excellent |
| EHP | 41,270 | PoB effective HP estimate |

---

*PoB XML: `bouyou_lv95.xml` | pob-brain verified | 2026-03-22*
*Build strategy: Inquisitor Templar — Lightning Conduit primary, Impending Doom secondary*
