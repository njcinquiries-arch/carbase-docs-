# 🎁 Card Packs & Gacha Mechanics

**Card Packs** in Carbase are how you unlock premium 3D card materials, Skia holographic shaders, particle effects, and garage customization items.

---

## 📦 Pack Tiers & Exact Pricing

All purchases are processed securely through Apple In-App Purchase and Google Play Billing:

| Pack Tier | In-App Price | Drop Pool | Target Value |
|---|---|---|---|
| 🥈 **Silver Pack** | **$2.00** *(or Daily PRO Claim)* | Common, Uncommon, Rare Skins | Min $15 – Max $1,000 |
| 🥇 **Gold Pack** | **$5.00** | Rare, Epic Material Shaders | Min $30 – Max $2,000 |
| 🔴 **Ruby Pack** | **$10.00** | Epic, Legendary Holographic Foils | Min $75 – Max $5,000 |
| 💎 **Diamond Pack** | **$20.00** | Guaranteed Legendary & Grail Shaders | Min $200 – Max $15,000 |

---

## ⚡ Volatility Events: Normal vs. Elevated Odds

Inside the Shop and Vault, players can inspect dynamic probability curves (`app/shop-odds.tsx`):

* **Normal Mode (Consistent Spread):** Standard drop distributions across all rarity buckets.
* **Elevated Mode (Special Events):** Higher risk variance that compresses mid-tier drops to dramatically boost the probability of hitting **Legendary and Grail Shaders** (such as *Diamond Ice*, *Crystal Glass*, and *Platinum Prestige*).

---

## 🎨 Binder Collection

Unlocked materials are permanently added to your personal **Collection Binder** (`app/collection.tsx`). You can hot-swap materials onto any car in your garage at zero additional cost.
