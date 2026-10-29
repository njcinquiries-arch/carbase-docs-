# 🪟 Liquid Glass & Intrinsic Component Architecture

CarBase combines Apple SwiftUI native views with React Native to create an ultra-tactile, fluid, and modern automotive interface. This document outlines the core UI components, glassmorphism systems, and layout ergonomics implemented across the platform.

---

## 💎 Native Apple SwiftUI Liquid Glass

Where supported on iOS 16+, CarBase leverages native SwiftUI glass containers (`@expo/ui/swift-ui`):

* **Interactive Material Response:** Utilizes `glassEffect({ glass: { variant: 'regular', interactive: true }, shape: 'capsule' })` for physical light refraction and dynamic blur.
* **Hybrid Host Integration:** Mounts SwiftUI buttons inside lightweight `Host` boundaries with explicit dimensions to guarantee tactile responsiveness and zero layout clipping.
* **Fallbacks for Multiplatform:** Seamlessly drops back to hardware-accelerated `expo-blur` (`BlurView`) and translucent rgba overlays on Android and older devices.

---

## 💊 Ergonomic Visitor Action Pills

When viewing another driver's public profile (`app/user-profile.tsx`), the primary visitor interactions are anchored by dual elongated action pills:

```
+------------------------------------+------------------------------------+
|          💬  Message               |          👥  Add Friend             |
+------------------------------------+------------------------------------+
```

* **Full-Width Symmetrical Span:** Computed dynamically as `Math.floor((width - 36 - 12) / 2)` (~175pt on modern iPhone displays) to stretch symmetrically across the screen gutters.
* **Human Interface Touch Target:** 48pt standard touch height with full capsule clipping and centered SF Symbol iconography.
* **Reactive State Tracking:** The Friend pill automatically toggles to an active checkmark (`✅ Friends`) with clear glass tint when friendship is confirmed.

---

## 👑 Liquid Glass Crew Rank Badges

In the profile hero identity card and Crew affiliation drawer, crew rankings are rendered with clean, un-tinted liquid glass:

* **No Background Color Tint:** Uses neutral translucent glass (`rgba(255, 255, 255, 0.08)` and subtle border `rgba(255, 255, 255, 0.18)`), eliminating legacy background color flooding.
* **High-Contrast Neutral Typography:** Text is rendered in crisp white (`#FFFFFF`) with 600 weight.
* **Native Emoji Rarity Hierarchy:** Hierarchy is instantly recognized via the emoji's native vibrant coloration:
  * 👑 **Crew Founder** / **Founder**
  * ⚡ **Admin** / **Officer**
  * 🔥 **Elite Builder**
  * 🏎️ **Driver** / **Member**

---

## 🌅 Atmospheric Banner Dissolve & Horizon Bleed

To eliminate harsh rectangular borders where the hero banner meets the dark profile body, CarBase employs a multi-stop atmospheric dissolve system:

1. **Top Status Scrim:** Dark gradient overlay (`rgba(0,0,0,0.65)` to `transparent`) ensuring Dynamic Island, clock, and battery icons remain legible.
2. **Deep Bottom Dissolve Gradient:** Spans 135pt up the banner with quadratic alpha easing (`rgba(5, 5, 7, 0.03)` → `0.15` → `0.42` → `0.74` → `0.94` → `#050507`), ensuring the bottom pixel matches the background with 100% color accuracy.
3. **Horizon Bleed Bridge:** A subtle 32pt `#050507` transition band placed across the banner-profile boundary that dissolves subpixel anti-aliasing seams.
4. **Ambient Scenery Spill:** An atmospheric light wash (`rgba(212, 165, 116, 0.08)` warm amber + `rgba(56, 189, 248, 0.04)` alpine blue) that casts the ambient colors of the banner down behind the driver's avatar and bio.

---

## 📑 4-Tab Profile Navigation

Profiles feature a streamlined horizontal tab bar with tactile switching and deep-linking support (`?tab=garage|stats|crew|more`):

* **🏎️ Garage:** Main vehicle showroom, build cards, and active project lineup.
* **📊 Stats:** Vehicle telemetry, dyno horsepower, acceleration benchmarks, and achievement progression.
* **🏁 Crew:** Affiliated car club roster, inception date, crew reputation (XP), and division standing (with minimalist, icon-free stat metric tiles).
* **📚 More:** Base Deck card catalog, collection milestones, and verified driver comments.

---

## 🛍️ Unified Shop & Base Bolts Store

The CarBase Shop modal (`app/shop-modal.tsx`) utilizes a unified, continuous vertical scroll architecture:

1. **Header Navigation:** Pinned safe-area navigation with user balance badge, gift modal access, and close controls.
2. **Horizontal Rip Packs Carousel:** Inertial roulette carousel displaying Silver, Gold, Ruby, and Diamond card packs with dynamic physics.
3. **Active Pack Inspection:** Interactive "What's Inside" preview, volatility odds breakdown, and glowing liquid glass purchase trigger.
4. **Purchase Base Bolts Section:** Positioned directly below the packs within the main scroll, offering tiered bolt packages ($4.99 to $49.99) with bonus multipliers and instant wallet top-ups.
