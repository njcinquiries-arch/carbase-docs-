# 🔧 Logging Modifications

The **Mod Log** is the core of your verified build record on Carbase. Every part you install or plan gets documented, AI-verified, and permanently timestamped to your build timeline.

Access it from your Car Detail page → **Mods Tab** → **Add Mod**, or via the **+** quick-action menu → **Log Mod**.

---

## Required Fields

| Field | Details |
|---|---|
| **Modification Name** | e.g. *Downpipe*, *Coilovers*, *Tune* |
| **Brand** | e.g. *Agency Power*, *KW Suspension*, *BMS* |
| **Category** | One of 8 categories (see below) |
| **How You Got It** | Online · In-Person · DIY/Fab |
| **Status** | Planned or Installed |

---

## 📦 Mod Categories

| Category | Affects Performance Stats |
|---|---|
| ⚡ **Software / Power** | ✅ Yes |
| 🔩 **Suspension & Chassis** | ✅ Yes |
| 🛑 **Braking** | ✅ Yes |
| 🌡️ **Cooling / Thermal** | ✅ Yes |
| 🔄 **Wheels & Tires** | ✅ Yes |
| 💨 **Aero / Weight Reduction** | ✅ Yes |
| 🎨 **Visual** | ❌ No |
| 🧰 **Utility** | ❌ No |

---

## 🛒 Acquisition Type & Verification Proof

How you acquired the part determines what proof is required:

### Online Purchase
* Enter the **Product URL** — Carbase validates it against 50+ authorized automotive merchant domains.
* **Auto-Fill**: Paste a product link and the app extracts the part title, brand, price, and part number automatically.
* URLs are screened against a blocklist of malware, scam sites, and URL shorteners for security.

### In-Person Purchase
* Upload a **Receipt Photo** — a clear image of your shop receipt or invoice.

### DIY / Fabricated
* **Installation Photo is required** — no receipt or URL needed, but photo evidence of the completed install must be attached.
* Note: DIY stat impact may be restricted since no product specs can be verified.

---

## 📊 Planned vs. Installed Status

### Planned Mods
Track your wishlist and build roadmap before spending:
* Set priority: **Next** · **Later** · **Someday**
* Log an estimated price and part number / SKU
* Shows in your Mods tab organized by priority queue

### Installed Mods
* **Installation Photo is mandatory** — a mod cannot be marked as installed without attached photo proof.
* Once saved as installed, the mod enters the build timeline and OVR Score calculation pipeline.

---

## 🤖 AI Performance Claim Verification

When you log claimed HP and torque gains, tap **"Verify with AI"**:

1. The AI evaluates your vehicle's make/model/year, the mod name, brand, category, and your claimed gains.
2. Returns a **realism verdict**: Realistic · Inflated · Implausible — with a confidence level (High / Medium / Low) and an explanation.
3. If your claims appear inflated:
   * Accept the AI's **suggested realistic values** (marked *Estimated*), or
   * Keep your own values (flagged as *User Entered* — visible to the community).

**Hard Ceilings (`MAX_REALISTIC_GAINS`):**
The system enforces hard limits on claimed gains by category regardless of what you enter — e.g., Cooling mods cap at +10hp, Aero caps at +15hp, Visual/Suspension/Braking mods contribute 0hp to performance calculations.

---

## ✅ Verification Status & Confidence Score

Every saved mod is assigned a verification status and confidence level:

| Status | How Achieved |
|---|---|
| ✅ **Verified** | Online link validated + AI confirms realistic gains |
| ⚠️ **Unverified** | No proof attached or link failed validation |
| 🚩 **Flagged** | AI determined claimed gains are unrealistic |

| Confidence | Condition |
|---|---|
| 🟢 **High** | Online verified URL + AI-confirmed realistic HP/torque |
| 🟡 **Medium** | Valid online link but no AI verification run |
| 🔴 **Low** | In-person receipt or DIY/unverified source |

Only **Verified** mods receive 100% OVR Score credit. Unverified and flagged mods appear on your timeline but contribute zero to your score until proof is attached.
