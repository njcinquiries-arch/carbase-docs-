# ⭐ OVR Score

The OVR Score is Carbase AI's proprietary rating system that measures your vehicle's overall performance potential. It is calculated out of a maximum of **100 points** across 5 distinct automotive categories.

***

## Baseline vs. Current Score

**Baseline Score** — Your vehicle's score straight from the factory. Every car starts here based on stock specs.

**Current Score** — Your live OVR Score reflecting all logged and verified modifications applied to your build.

***

## Modification Timeline

Every mod you add is timestamped and logged to your build history. Your OVR Score timeline shows exactly how your build has evolved — from stock to where it is today.

***

## How the Score Is Calculated

The OVR Score is built from 5 weighted categories. Each category contributes a portion of the total 100-point maximum.

***

### 🔥 1. Power Output — 30 pts

Based on the vehicle's horsepower (HP).

| Horsepower     | Points |
| -------------- | ------ |
| ≥ 700 HP       | 30     |
| ≥ 500 HP       | 25     |
| ≥ 350 HP       | 20     |
| ≥ 250 HP       | 15     |
| ≥ 150 HP       | 10     |
| < 150 HP       | 5      |

***

### ⚡ 2. Acceleration — 25 pts

Based on 0–60 mph time in seconds.

| 0–60 mph Time  | Points |
| -------------- | ------ |
| ≤ 2.5s         | 25     |
| ≤ 3.5s         | 22     |
| ≤ 4.5s         | 18     |
| ≤ 6.0s         | 12     |
| ≤ 8.0s         | 6      |
| > 8.0s         | 2      |

***

### ⚖️ 3. Power-to-Weight Ratio — 20 pts

Calculated as HP per ton `(HP ÷ (Weight in lbs ÷ 2000))`.

| HP per Ton     | Points |
| -------------- | ------ |
| ≥ 400 HP/ton   | 20     |
| ≥ 300 HP/ton   | 17     |
| ≥ 200 HP/ton   | 14     |
| ≥ 100 HP/ton   | 9      |
| < 100 HP/ton   | 4      |

***

### 🚗 4. Traction Layout — 10 pts

Based on drivetrain type.

| Drivetrain | Points |
| ---------- | ------ |
| AWD        | 10     |
| 4WD        | 9      |
| RWD        | 8      |
| FWD        | 5      |

***

### 🏆 5. Heritage & Prestige — 15 pts

Based on brand tier and halo vehicle status.

| Brand Tier                                      | Points |
| ----------------------------------------------- | ------ |
| Halo Vehicles (e.g. GT-R Nismo, Bugatti, etc.)  | 15     |
| Premium Exotic (e.g. Ferrari, Lamborghini)       | 12     |
| Premium Tier (e.g. BMW, Porsche, Mercedes-AMG)  | 10     |
| Enthusiast Japanese (e.g. Toyota, Mazda, Honda) | 8      |
| Standard Tier                                   | 6      |

***

## The Formula

```
OVR Score = min(100, Power + Acceleration + Power-to-Weight + Drivetrain + Prestige)
```

The score is capped at **100** — no vehicle can exceed the maximum regardless of individual category scores.

***

## ⚠️ Important Disclaimer

The OVR Score is a proprietary estimate and opinion metric — not a certified appraisal, safety rating, or financial valuation. Do not rely on it for purchase, sale, insurance, or financing decisions.
