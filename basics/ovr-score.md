# ⭐ OVR Score

The OVR Score is Carbase AI's proprietary rating system — a programmatic evaluation of your vehicle's performance potential, build depth, and verified modification history. Every car on the platform carries two scores: a **Baseline** and a **Current**.

***

## Baseline vs. Current Score

**📦 Baseline Score**
Your vehicle's score straight from the factory. Calculated purely from stock specs — horsepower, acceleration, drivetrain, power-to-weight ratio, and brand heritage. This never changes. It reflects what the manufacturer built.

**🔧 Current Score**
Your live OVR Score. It starts at your Baseline and climbs as you log and verify modifications to your build. The more you build, the higher it goes — up to the platform maximum of **100**.

> A stock Ferrari and a built Civic can both score 100. The difference is how you got there.

***

## How the Baseline Is Calculated

The Baseline OVR Score is built from **5 weighted performance categories**, totaling a maximum of 100 points.

***

### 🔥 1. Power Output — 30 pts

| Horsepower   | Points |
| ------------ | ------ |
| ≥ 700 HP     | 30     |
| ≥ 500 HP     | 25     |
| ≥ 350 HP     | 20     |
| ≥ 250 HP     | 15     |
| ≥ 150 HP     | 10     |
| < 150 HP     | 5      |

***

### ⚡ 2. Acceleration — 25 pts

| 0–60 mph Time | Points |
| ------------- | ------ |
| ≤ 2.5s        | 25     |
| ≤ 3.5s        | 22     |
| ≤ 4.5s        | 18     |
| ≤ 6.0s        | 12     |
| ≤ 8.0s        | 6      |
| > 8.0s        | 2      |

***

### ⚖️ 3. Power-to-Weight Ratio — 20 pts

Calculated as `HP ÷ (Weight in lbs ÷ 2000)` (HP per ton).

| HP per Ton    | Points |
| ------------- | ------ |
| ≥ 400 HP/ton  | 20     |
| ≥ 300 HP/ton  | 17     |
| ≥ 200 HP/ton  | 14     |
| ≥ 100 HP/ton  | 9      |
| < 100 HP/ton  | 4      |

***

### 🚗 4. Traction Layout — 10 pts

| Drivetrain | Points |
| ---------- | ------ |
| AWD        | 10     |
| 4WD        | 9      |
| RWD        | 8      |
| FWD        | 5      |

***

### 🏆 5. Heritage & Prestige — 15 pts

| Brand Tier                                        | Points |
| ------------------------------------------------- | ------ |
| Halo Vehicles (GT-R Nismo, Bugatti, etc.)         | 15     |
| Premium Exotic (Ferrari, Lamborghini, McLaren)    | 12     |
| Premium Tier (BMW M, Porsche, Mercedes-AMG)       | 10     |
| Enthusiast Japanese (Toyota, Mazda, Honda, Subaru)| 8      |
| Standard Tier                                     | 6      |

***

### The Baseline Formula

```
Baseline OVR = min(100, Power + Acceleration + Power-to-Weight + Drivetrain + Prestige)
```

***

## How Mods Boost Your Current Score

Once your baseline is set, modifications push your Current Score above it. Every mod you log is evaluated by Carbase AI's built-in performance engine, which maps keywords from your build log to known performance gains.

### How Mod Verification Works

Carbase AI doesn't just take your word for it. Every modification goes through a **3-layer verification process** before it counts toward your Current Score:

**1. 🧾 Receipt Upload**
Upload a purchase receipt from the shop, dealer, or retailer that supplied the part. Carbase AI reads and validates the document.

**2. 🔗 Product Link Submission**
Submit the direct product URL — from any major aftermarket retailer (Amazon, Summit Racing, TireRack, manufacturer sites, etc.). Our system cross-references the link against known part databases to confirm the modification is real and compatible with your vehicle.

**3. 🤖 AI Verification**
Carbase AI's built-in AI reviews your receipt, product link, and mod description together. It confirms authenticity, flags inconsistencies, and approves or flags the modification for review. Approved mods are permanently logged to your build timeline.

> Cosmetic and handling mods (wraps, coilovers, wings) are verified the same way — they just don't affect your HP/Torque figures.

***

## Performance Boost Model

When a mod is verified, Carbase AI's engine runs a **fuzzy keyword parser** against the MOD\_IMPACT\_MAP to extract the performance gains for that modification. Total gains are summed across all verified mods:

```
ΔHP_total    = ΔHP₁ + ΔHP₂ + ... + ΔHPₙ
ΔTorque_total = ΔTorque₁ + ΔTorque₂ + ... + ΔTorqueₙ
```

### Mod Impact Reference Table

| Modification                          | ΔHP      | ΔTorque    |
| ------------------------------------- | -------- | ---------- |
| 🌀 Turbocharger                        | +100 HP  | +120 lb-ft |
| ⚡ Supercharger                        | +80 HP   | +90 lb-ft  |
| 💨 Nitrous System                      | +75 HP   | +50 lb-ft  |
| 🖥️ ECU Tune / Remap                   | +40 HP   | +50 lb-ft  |
| 🔩 Camshaft Profile Upgrade            | +30 HP   | +20 lb-ft  |
| 🔧 Downpipe Upgrade                    | +25 HP   | +30 lb-ft  |
| 🔊 Exhaust Upgrade                     | +15 HP   | +20 lb-ft  |
| 🌬️ High-Flow Intake                   | +15 HP   | +10 lb-ft  |
| ❓ Unmapped Custom Mod                 | +5 HP    | +5 lb-ft   |
| 🎨 Handling / Cosmetic (coilovers, wraps, wings) | +0 HP | +0 lb-ft |

***

## Overall Rating Boost from Mods

Verified modifications also directly boost your **Overall Score** shown on the front of your Car Card. The boost is calculated based on your total mod count:

```
ΔRating = min(3, Round(Mod Count × 0.5))
Final OVR = min(100, Baseline + ΔRating)
```

The modification boost is **capped at +3 points** to preserve balance between stock vehicles and custom builds. This means the Baseline still matters — but a well-documented build always edges out a stock car at the same baseline.

| Verified Mods | Rating Boost |
| ------------- | ------------ |
| 1–2 mods      | +1           |
| 3–4 mods      | +2           |
| 5+ mods       | +3 (max)     |

***

## HUD Studio Class Rating

Every build on Carbase AI also carries a **Class Rating** — a letter grade displayed on your Car Card's HUD that reflects the total horsepower gained from verified modifications.

| Class | ΔHP Total Required         |
| ----- | -------------------------- |
| 🟠 **S** | ≥ 200 HP gained          |
| 🔵 **A** | 100 – 199 HP gained      |
| 🟢 **B** | 40 – 99 HP gained        |
| 🟡 **C** | 10 – 39 HP gained        |
| ⚪ **D** | < 10 HP gained (stock)   |

A stock vehicle with no modifications starts at **Class D**. Add a turbo and an ECU tune and you're already hitting **Class A**. Stack a full build and earn your **S Class**.

***

## Modification Timeline

Every verified mod is permanently timestamped to your build history. Your OVR Score timeline shows the exact progression of your build — every part, every boost, every milestone — visible to the community on your Car Card.

***

## ⚠️ Disclaimer

The OVR Score, Class Rating, and all performance figures are proprietary estimates generated from user-submitted and AI-verified data. They are not certified mechanical appraisals, safety ratings, or financial valuations. Always consult a qualified mechanic before making modifications to your vehicle.
