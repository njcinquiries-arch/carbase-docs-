# 🚗 Your Car Detail Page

The **Car Detail** page is the full command center for each vehicle in your garage. Tap any car in your Garage tab to open it.

---

## Hero Stage Header

At the top of the page:
* **Interactive 3D Car Card** — gyroscope-enabled tilt, dynamic stage background lighting, and active holographic shader.
* **Liquid Toggle** — switch between **Current** build stats (with all verified mod gains applied) and the original **OEM Baseline** specs side by side.
* **Verification Badge** — shows VIN Verified ✅, Unverified ⚠️, or a "Verify Now" prompt to initiate VIN verification.
* **Powertrain Badge** — Combustion or EV.
* **Rank Tier Badge** — Rookie through Signature.
* **Owner Menu (3 dots)** — Rename car, Update photo, Share card, Order Car Code sticker, Delete vehicle.

---

## The 4 Tabs

### 📊 Overview Tab

A full snapshot of your vehicle's performance data:

* **Performance Stats Grid**: Live horsepower, torque, curb weight, 0–60 mph, and power-to-weight ratio — showing both the current build figure and the delta gain over baseline (e.g. `+47 hp`). Each stat shows its data source: `OEM`, `Estimated`, or `User Entered`.
* **Vehicle Specifications**: Year, Make, Model, Trim, Powertrain, Drivetrain, Engine config, estimated ¼ mile and top speed, build status (Stock / Modified), installed mod count, planned mod count.
* **Exhaust Note Player**: Animated waveform audio player with position scrubber, play/pause, replace, and record-engine controls. Plays your recorded or uploaded exhaust audio.
* **Build Intent Card**: Your primary goal, use case, and risk preference set during car creation.
* **AI Rating Analysis**: Confidence rating, points delta from mods, AI reasoning narrative explaining your OVR score, comparable real-world vehicles, and rank tier description.
* **"Ask Advisor About This Car"**: One tap launches the AI Advisor pre-loaded with all your vehicle specs and installed mods — no need to explain your setup manually.

---

### 🔧 Mods Tab

Your full modification roadmap organized by build stage:

**Planned Mods (Queued Build Roadmap):**
* **Next** — Immediate upcoming parts
* **Later** — Mid-term planned parts
* **Someday** — Long-term wish list items

Each planned mod shows: part name, brand, part number, estimated price, and priority.

**Total plan cost** is calculated and displayed as a running budget summary (`Plan total · $X`).

**Installed Mods (Completed Build):**
Every verified installed mod shows:
* Part name, brand, and category
* Stat impact: `+X hp / +Y lb-ft` with source label (user entered / estimated)
* Verification badge (✅ Verified / ⚠️ Unverified / 🚩 Flagged)
* Product URL link (if applicable)

---

### 📸 Showcase Tab

Your vehicle's media gallery:
* **Free tier**: 4 images · 1 video
* **Carbase PRO**: 9 images · 4 videos
* Tap **Enter Showcase** for a full-screen immersive media viewer.
* Add images and video clips directly from your camera roll.

---

### 📅 Timeline Tab

A permanent, chronological log of your entire build history from day one:

```
● Card Created — [Date]
│
● Intake Installed (+22 hp / +18 lb-ft) — [Date]    ✅ Verified
│
● Rank Changed: Rookie → Amateur — [Date]
│
● Downpipe Installed (+31 hp / +28 lb-ft) — [Date]  ✅ Verified
│
● Exhaust Note Updated — [Date]
│
● ECU Tune Installed (+45 hp / +40 lb-ft) — [Date]  ⚠️ Unverified
```

Each timeline event includes: event description, photo thumbnail (if applicable), formatted date, and stat deltas. Events tracked include: card creation, mod installs/removals, rank tier changes, photo updates, and build intent adjustments.
