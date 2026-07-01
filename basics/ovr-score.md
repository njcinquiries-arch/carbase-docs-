# ⭐ OVR Score

The OVR Score is Carbase AI's proprietary vehicle rating — a number between 0 and 100 that reflects how well a vehicle performs **within its intended role**. It is not a flat performance leaderboard. A Toyota 4Runner and a Lamborghini Huracán can both earn respectable scores — for completely different reasons.

{% hint style="warning" %}
**Note:** The formulas, weights, and coefficients detailed below are simplified conceptual representations used to illustrate the underlying principles of the rating model. The actual production Carbase AI engine employs a proprietary, non-linear multi-factor model, dynamic lookup maps, and private tuning constants to compute final scores.
{% endhint %}

***

## Baseline vs. Current Score

**📦 Baseline Score**
Your vehicle's score as it left the factory. Calculated from stock specs and evaluated against its classified role. This never changes.

**🔧 Current Score**
Your live score after verified modifications are applied. Mods are analyzed, weighted, and factored in — pushing your Current Score above your Baseline based on what you've actually built and proven.

***

## How Scoring Works — Role-Aware Evaluation

Instead of a flat performance scale, Carbase AI uses a **Dynamic Domain Weighting Model**. Every vehicle is first classified by its role, then evaluated across 7 domains. The weight each domain carries shifts based on what the vehicle was built to do — ensuring off-road trucks are not penalized for poor cornering, and supercars are not penalized for lack of cargo capacity.

The conceptual formula:

```
R = min(100, Σ (Sd × Wd,role))
```

Where `Sd` is the vehicle's raw score in each domain, and `Wd,role` is the weight applied to that domain for the vehicle's classified role. All weights sum to 1.0.

***

## The 7 Evaluation Domains

| Domain | What It Measures |
| ----------- | ------------------------------------------------- |
| 🏎️ Performance | Power, acceleration, handling, track capability |
| 🛡️ Safety | Braking, structural integrity, driver aids |
| 🔩 Reliability | Engine longevity, build quality, service history |
| 🛋️ Comfort | Cabin noise, ride quality, interior refinement |
| ⛽ Efficiency | Fuel economy, emissions, powertrain efficiency |
| 📦 Utility | Cargo capacity, towing, practicality |
| 🎯 Cohesion | How well all systems work together as a package |

***

## Dynamic Weighting Matrix

| Vehicle Role | Performance | Safety | Reliability | Comfort | Efficiency | Utility | Cohesion |
| -------------------- | ----------- | ------ | ----------- | ------- | ---------- | ------- | -------- |
| Utility / Off-Road | 0.05 | 0.20 | 0.25 | 0.10 | 0.05 | 0.25 | 0.10 |
| Luxury Sedan / Daily | 0.10 | 0.20 | 0.15 | 0.25 | 0.15 | 0.10 | 0.05 |
| Supercar / Hypercar | 0.45 | 0.10 | 0.05 | 0.05 | 0.05 | 0.05 | 0.25 |

***

## Case Studies — Utilization-Based Ratings

### 🏔️ Off-Road Utility SUV — Toyota 4Runner TRD Pro

**Role weights:** Heavy emphasis on Utility (0.25) and Reliability (0.25). Low emphasis on Performance (0.05) and Efficiency (0.05).

**Domain scores:**

| Domain | Score | Why |
| ----------- | ----- | ---- |
| 🏎️ Performance | 38/100 | Not built for speed — modest HP, slow acceleration |
| 🛡️ Safety | 74/100 | Solid crash ratings, decent driver aids |
| 🔩 Reliability | 96/100 | One of the most proven powertrains in automotive history |
| 🛋️ Comfort | 62/100 | Capable interior, but dated refinement and road noise |
| ⛽ Efficiency | 32/100 | Poor fuel economy — a known tradeoff for the platform |
| 📦 Utility | 94/100 | Class-leading towing, off-road articulation, cargo capacity |
| 🎯 Cohesion | 88/100 | Everything works exactly as intended for its role |

**Baseline Score: ~66 OVR**
The role-aware model protects the 4Runner from being crushed by poor fuel economy and speed metrics. However, its aerodynamic profile, weight, and highway comfort limits act as a structural ceiling.

**With Verified Off-Road Mods** (lift kits, heavy-duty suspension, air lockers): climbs into the **mid-70s (74–76 OVR)**.

**Capped Ceiling:** The system ensures a utility truck can never reach Elite status (80+). True Elite is reserved for vehicles with higher multi-domain capability. This keeps the scoring honest.

***

### 🏎️ High-Performance Supercar — Lamborghini Huracán

**Role weights:** High priority on Performance (0.45) and Cohesion (0.25). Low priority on Utility (0.05) and Comfort (0.05).

**Domain scores:**

| Domain | Score | Why |
| ----------- | ----- | ---- |
| 🏎️ Performance | 98/100 | 630HP, 2.9s 0-60, near-perfect lateral G figures |
| 🛡️ Safety | 72/100 | Strong braking and stability systems, limited passive safety |
| 🔩 Reliability | 58/100 | Exotic maintenance requirements, higher service frequency |
| 🛋️ Comfort | 55/100 | Firm, loud, and unforgiving — intentionally so |
| ⛽ Efficiency | 28/100 | 13 MPG combined — expected at this power level |
| 📦 Utility | 20/100 | Essentially zero cargo, two seats, no practicality |
| 🎯 Cohesion | 96/100 | Every system — aero, chassis, powertrain — built to one purpose |

**Baseline Score: low-to-mid 90s OVR**
The poor Utility and Comfort scores barely register under supercar role weighting. Performance and Cohesion dominate. The exotic maintenance tradeoffs keep it honest — a perfect 100 remains out of reach.

***

## Modification Impact & Rating Boost

When you add mods, Carbase AI's engine analyzes each modification and assigns it to a functional category. Each category carries a performance coefficient contributing to your total power and torque gains.

### 📸 Mod Verification Requirement

Mods must be verified to contribute to your OVR Score. Verification requires at least one of the following:

* 🧾 **Receipt** — purchase receipt from the shop or retailer
* 🔗 **Product Link** — direct URL to the part from any major aftermarket retailer
* 📸 **Installation Photo** — photo proof of the mod on your vehicle

| Verification Status | Score Impact |
| ------------------- | ------------ |
| ✅ Verified | 100% performance credit applied to OVR Score |
| ⚠️ Unverified | Zero score credit — appears on timeline as flagged, does not affect OVR |

> An unverified mod is visible on your build timeline so the community can see what you claim — but it counts for nothing until proven. Verification is what separates a real build from a spec sheet.

***

## HUD Studio Class Rating

| Class | Build Level |
| ----- | ----------------------------------------- |
| 🟠 **S** | Extreme / Exotic — major power adders working in unison |
| 🔵 **A** | Forced Induction / Advanced — heavy bolt-ons or single forced-induction |
| 🟢 **B** | Moderate Bolt-Ons — typical street builds (intake, exhaust, tune) |
| 🟡 **C** | Entry Level — minor supporting upgrades |
| ⚪ **D** | Stock — no meaningful performance modifications logged |

### Tuning Case Studies

**🔧 The Bolt-On Street Build**

* Mods: 1 verified intake, 1 verified exhaust, 1 **unverified** ECU tune
* The intake and exhaust receive full credit. The unverified ECU tune appears on the build timeline marked ⚠️ unverified — it adds zero to the OVR Score until verified with a receipt, link, or photo.
* Result: Intake + exhaust gains only → **Class B**, minor rating boost. The tune is visible on the timeline but does nothing until proven.

**🚀 Max-Spec Track Build**

* Mods: Verified twin-turbos, verified ECU tune, verified nitrous, verified downpipe, verified aero splitter, unverified underglow
* All 5 performance mods are fully credited. The unverified underglow appears on the timeline as ⚠️ unverified — cosmetic or not, it contributes zero to the score.
* Result: Twin-turbo synergy with nitrous and supporting software pushes past the upper threshold → **Class S**, maximum rating boost applied

***

## Public Showroom Trust & VIN Verification

```
[ Public Showroom Card ]
+------------------------------------+
| 2023 Lamborghini Huracán           |
| Overall: 92  |  Rank: Elite        |
|                                    |
|  [⚠️ UNVERIFIED SPECS & OWNER]     |
+------------------------------------+
```

| Status | Badge | What It Means |
| ------ | ----- | ------------- |
| ✅ VIN Verified | 🟢 Verified Owner | VIN decoded, ownership confirmed, specs are 100% authentic |
| ⚠️ Self-Reported | 🟡 Unverified Specs & Owner | Manually entered, unconfirmed against registration databases |

### Showroom Case Studies

**Case A — Verified Entry**
A user adds a 2021 Porsche 911 Turbo S and completes VIN verification. The card publishes with a clean premium layout and a green Verified Owner badge. The community knows with certainty the car and specs are genuine.

**Case B — Self-Reported Entry**
A user manually claims a 2023 Lamborghini Huracán STO but skips VIN verification. The card is still visible publicly in the showroom — but carries a prominent yellow "Unverified Specs & Owner" banner. The community can see the card and the build, but knows the specs and ownership have not been confirmed. Visibility is not restricted — transparency is enforced instead.

***

## Modification Timeline

Every verified mod is permanently timestamped to your build history. Your OVR Score timeline shows the full progression of your build — every part logged, every boost earned — visible to the community on your Car Card.

***

## ⚠️ Disclaimer

The OVR Score, Class Rating, and all performance figures are proprietary estimates generated from user-submitted and AI-verified data. They are not certified mechanical appraisals, safety ratings, or financial valuations. Always consult a qualified mechanic before making modifications to your vehicle.
