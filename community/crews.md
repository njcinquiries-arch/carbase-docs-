# 👥 Car Crews & Clubs

**Crews** in Carbase are dedicated car clubs engineered for builders, enthusiasts, and local car meets to connect, chat, and climb leaderboards together.

---

## 🏎️ Crew Categories

When founding a new crew (`app/group-create.tsx`), founders select a category focus:

| Category | Focus Area |
|---|---|
| 🇯🇵 **JDM** | Japanese Domestic Market platforms (Nissan, Toyota, Honda, Subaru, Mazda) |
| 🇪🇺 **EURO** | European Performance & Precision (BMW, Porsche, Audi, Mercedes-AMG, VW) |
| 🦅 **MUSCLE** | American V8, Drag, and Classic Muscle (Ford, Chevrolet, Dodge) |
| ⚡ **EV** | High-Voltage & Electric Performance (Tesla, Rivian, Lucid, Porsche Taycan) |
| 🏔️ **OFF-ROAD** | Overlanding, Trail Rigs, Rock Crawlers & Lifted Trucks |
| 🏁 **TRACK** | Time Attack, Autocross, HPDE, Road Course Builds |
| 🎨 **AESTHETIC / STANCE** | Fitment, Air Suspension, Show Car Builds, Livery Designs |
| 📍 **LOCAL / REGIONAL** | City and state-based geographic enthusiast clubs |

---

## 💬 Social Hub & Real-Time Features

* **Live Crew Chat & 1-on-1 Direct Messaging (`contexts/MessagingContext.tsx`):** Send real-time messages with photo attachments and embedded interactive Car Card preview widgets.
* **Transformation Feed:** Post side-by-side Before/After build updates with "Helpful" and "Saved" upvote mechanics.
* **Daily Crew Challenges:** Collaborative daily tasks rewarding both personal User XP and collective Crew standing.
* **Optional Live GPS Meetup Map (`expo-location` & `react-native-maps`):** Three granular location privacy tiers (`live`, `approximate`, `private`) for tracking convoy drives and locating car meetups.
