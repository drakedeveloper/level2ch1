# ⚔️ Hunter Association — Fight Predictor System

A rule-based combat simulation web app that predicts the outcome of a duel between two Nen users. No randomness — every result is fully calculated and explained step by step.

## Launch

Just open the file in your browser:

```
double-click fight-predictor.html
```

No server, no install, no dependencies.

## How It Works

Fill in both fighters' names, Nen types, and base stats using the sliders, then click **Simulate Duel**.

The engine runs four steps:

**1. Weighted Base Score**
Each of the 7 stats is multiplied by its combat weight and summed into a single score:

| Stat | Weight |
|---|---|
| Speed | 0.20 |
| Strength | 0.18 |
| Intelligence | 0.15 |
| Durability | 0.14 |
| Aura Capacity | 0.13 |
| Aura Control | 0.13 |
| Experience | 0.07 |

**2. Nen Type Advantage**
Types follow a circular advantage system based on HxH lore:

```
Enhancement → Emission → Transmutation → Conjuration → Manipulation → Enhancement
```

The favored type receives a ×1.15 multiplier. Specialization is a wildcard and always gets ×1.10 regardless of the opponent's type.

**3. Final Score**
`Final Score = Base Score × Nen Multiplier`

**4. Win Probability**
Each fighter's share of the combined score pool gives their win probability as a percentage.

## Output

- **Winner banner** with confidence level (close / decisive / etc.)
- **Score comparison bar** showing both final scores side by side
- **Per-stat breakdown** for each fighter with contribution per stat
- **Stat-by-stat comparison** with dual progress bars
- **Animated calculation log** showing every arithmetic step in full
