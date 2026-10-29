# 🏛️ The Mint • Collector Dex & Automotive Vault

**The Mint** is CarBase's automotive card-creation hub, cold-vault registry, and decentralized collector economy. It bridges physical automotive culture with digital collectible trading cards, computer-vision spotting, and social prestige.

---

## 🎯 Core Objectives & Capabilities

The Mint turns real-world car spotting, vehicle ownership, and custom builds into a gamified, graded digital card collection:

1. **AI-Powered Spotter Camera:** Point your phone camera at any vehicle in the wild to instantly detect make, model, trim, and visible modifications—minting an official collector card on the spot.
2. **Base Dex (Collector Registry):** An automotive Pokédex that catalogs factory production models, legendary tuners, and 1-of-1 hypercars across international car cultures.
3. **Live Auctions & Dex Trading:** A community-driven marketplace powered by **Base Bolts** where drivers can list, bid on, and trade rare cards, custom holographic skins, and build cards.
4. **Prestige Multipliers & Cold-Vault Honors:** Earn compounding multipliers based on your garage horsepower, spotting accuracy, and collector streaks.

---

## 📸 AI Spotter Camera

The Spotter Camera (`components/SmartAISpotterModal.tsx`) utilizes high-speed automotive machine vision to evaluate vehicles in real time:

* **Instant Vehicle Recognition:** Identifies chassis code, year bracket, factory color, and aero packages.
* **Mod Spotting Engine:** Scans wheels, exhaust tips, suspension drops, carbon aero, and widebody kits.
* **Auto-Grading & Rarity Assignment:** Assigns an intrinsic **OVR rating** and rarity tier (Common, Uncommon, Rare, Epic, Legendary, Grail, Mythic) upon scan completion.
* **Spotter Card Minting:** Creates a unique collectible card that permanently records the spotter's handle, date, GPS coordinates, and vehicle spec.

---

## 🗂️ The Base Dex Catalog

The **Base Dex** acts as the central encyclopedia and collector binder for every vehicle in CarBase:

* **Category Completion:** Track your discovery progress across categories including *JDM Legends*, *Euro Precision*, *American Muscle*, *Track Day Exotics*, *Vintage Classics*, and *Off-Road Warriors*.
* **Interactive 3D Card Inspection:** Flip, rotate, and tilt minted cards with realistic lighting, gyroscopic parallax, and metallic foil reflections.
* **Cold-Vault Staking:** Safely lock cards in your digital cold vault to preserve condition and accrue continuous collector XP.

---

## ⚖️ Live Auctions & Market Exchange

Drivers can buy, sell, and auction cards through the integrated Dex Auction House:

* **Live Bidding Engine:** Real-time countdowns, anti-snipe extensions, and instant bolt escrow locking.
* **Buy It Now (BIN):** Instant settlement for fixed-price rare cards and exclusive holographic skins.
* **Bolts Economy:** Transparent fee structure denominated in **Base Bolts**, rewarding active community participants.

---

## 🏆 Mint Badges & Honors

Specialized honors awarded for high-precision spotter scans, rare car curation, and cold-vault milestones:

| Badge Title | Category | Requirements | Base Bolts Reward |
|---|---|---|---|
| 🦅 **Apex Spotter** | Spotting | 50 verified AI spotter scans with 95%+ precision | +500 Bolts |
| 👑 **Grail Curator** | Curation | Mint or hold 3+ Grail or Mythic cards in your vault | +1,200 Bolts |
| ❄️ **Cold Vault Master** | Staking | Stake 10+ legendary builds for 30 consecutive days | +800 Bolts |
| ⚡ **Dex Completionist** | Catalog | Achieve 100% completion in any regional category | +2,500 Bolts |
| 💎 **Mint Patron** | Economy | Complete 25 successful trades or auctions | +1,000 Bolts |

---

## 🔮 Liquid Glass Vault Blob Interaction

The Mint interface features Apple SwiftUI-native **Liquid Glass Vault Blobs** (`components/LiquidGlassVaultBlob.tsx`):

* **Interactive Material Response:** Smooth haptic feedback and dynamic fluidity when opening and closing the vault.
* **Ambient Lighting:** Adapts glow colors based on the highest rarity item held in the user's active session.
* **Direct Navigation:** One-tap toggle between camera spotting, catalog inspection, and live marketplace auctions.
