# Server-Driven UI (SDUI) — Complete Resource Guide & Learning Plan
### For Android Developers (Kotlin + Jetpack Compose)
*Curated for Tarun Sharma — May 2026*

---

## Table of Contents
1. [GitHub Repositories](#github-repositories)
2. [Official Engineering Blogs from Big Companies](#official-engineering-blogs)
3. [Articles & Blog Posts (Medium / Dev.to / ProAndroidDev)](#articles--blog-posts)
4. [YouTube Videos & Conference Talks](#youtube-videos--conference-talks)
5. [Documentation & Reference Sites](#documentation--reference-sites)
6. [Podcasts](#podcasts)
7. [Other Resources](#other-resources)
8. [🗺️ 12-Week Learning & Implementation Plan](#️-12-week-learning--implementation-plan)

---

## GitHub Repositories

### ⭐ Must-Study (Android / Kotlin)

| Repo | Stars | What you'll learn |
|------|-------|-------------------|
| [skydoves/server-driven-compose](https://github.com/skydoves/server-driven-compose) | ⭐⭐⭐ | **Best starting point.** Full SDUI with Jetpack Compose + Firebase Realtime DB. Covers rendering protocols, action handlers, versioning, and component design systems. Uses MVVM + Hilt + Retrofit. Perfect match for your AetheraAdmin stack. |
| [arrazyfathan/server-driven-ui](https://github.com/arrazyfathan/server-driven-ui) | ⭐⭐ | Concise, beginner-friendly SDUI example with Jetpack Compose. Good for understanding the core rendering loop before diving into larger projects. |
| [tchigher/beagle](https://github.com/tchigher/beagle-1) | ⭐⭐ | Beagle — a full SDUI framework originally by Zup IT. Kotlin on both backend and client. Uses Moshi for deserialization. Learn how a production-grade SDUI framework is structured end-to-end. |
| [Kotlin SDUI with Hilt + Navigation](https://github.com/topics/server-driven-ui) (search topic) | — | Browse the `server-driven-ui` GitHub topic to discover fresh repos with Hilt, Navigation 3, and Compose Multiplatform implementations. |

### Cross-Platform / Framework Reference

| Repo | What you'll learn |
|------|-------------------|
| [csmets/Server-Driven-UI](https://github.com/csmets/Server-Driven-UI) | Full-stack SDUI framework with GraphQL compositor, template server, and React client. Teaches the backend side — how a server actually generates UI schemas. Essential for understanding the full picture. |
| [MobileNativeFoundation/discussions #47](https://github.com/MobileNativeFoundation/discussions/discussions/47) | Not a repo but a goldmine — engineers from Airbnb, Lyft, Lyft, Wise, and startups share their real SDUI battle stories, code patterns, and architecture decisions. |
| [nicklockwood/Euclid](https://github.com/nicklockwood/Euclid) *(iOS reference)* | iOS SwiftUI SDUI reference if you ever need to go cross-platform with KMP. |

---

## Official Engineering Blogs

These are the **canonical real-world case studies** — read these like textbooks.

### 🏆 Tier 1 — Must Read (The Founding Papers)

1. **Airbnb — "A Deep Dive into Airbnb's Server-Driven UI System"**
   - 🔗 https://medium.com/airbnb-engineering/a-deep-dive-into-airbnbs-server-driven-ui-system-842244c5f5
   - Author: Ryan Brooks
   - This is *the* canonical paper for SDUI in mobile. Covers their Ghost Platform, how they serve Android + iOS + Web from the same schema, component versioning, and A/B testing at scale. Every SDUI system traces back to this.

2. **Swiggy — "A Deep Dive into Dynamic Widget: Swiggy's Server-Driven UI System"**
   - 🔗 https://bytes.swiggy.com/a-deep-dive-into-dynamic-widget-swiggys-server-driven-ui-system-92cdc3b16ec6
   - This is exactly the system you noticed in the Swiggy app. Covers how Swiggy uses Litho + SDUI for the home feed, location-based widgets, and dynamic banners. Real Indian context.

3. **Netflix — "Server-Driven UI for Mobile and Beyond"** (QCon London 2024)
   - 🔗 https://www.infoq.com/presentations/server-ui-mobile/
   - Staff Engineer Christopher Luu explains Netflix's UMA (Universal Messaging Alert) system, the spectrum of SDUI, backwards compatibility via GraphQL, and how they extended SDUI to TV + Web beyond just mobile.

4. **Lyft — "Canvas: A Server-Driven Framework for Mobile"**
   - 🔗 https://eng.lyft.com/canvas-a-new-way-for-lyft-to-describe-mobile-uis-e2de28d6bb88
   - Lyft's Canvas uses Protocol Buffers instead of JSON for a compact binary format. Learn why they chose protobuf, how they define primitives (buttons, layouts, action callbacks), and their versioning strategy.

### 🏅 Tier 2 — Company-Level Case Studies

5. **Reddit — Adopts SDUI for New Feed Architecture**
   - 🔗 https://www.infoq.com/news/2023/09/reddit-feed-server-driven-ui/
   - Reddit rebuilt their 6-year-old feed codebase (originally Objective-C) using SDUI. Result: home feed 12% faster to load. Learn how they reworked their GraphQL API response structure.

6. **DoorDash — "Mosaic: Server-Driven UI"**
   - 🔗 Search "DoorDash Mosaic server driven UI engineering blog"
   - DoorDash's Mosaic system — reduces time to deliver new banners and tags to under a day, modifications in less than an hour.

7. **Doist (Todoist) — "Server-Driven UI from a Mobile Perspective"**
   - 🔗 https://doist.dev/posts/server-driven-ui-from-a-mobile-perspective
   - Excellent balanced perspective from a smaller company. Covers the tradeoffs honestly, how they built their own SDUI SDK, and platform parity across Android + iOS.

8. **Q42 — "One Code to Rule Them All: Android Server Driven UI"**
   - 🔗 https://engineering.q42.nl/android-server-driven-ui/
   - Deep Android-focused case study. Uses Kotlin sealed classes as the type hierarchy, covers the full data → business logic → render flow. Explains how even local DB sync works differently with SDUI.

9. **Mercari — "Server-Driven UI for Marketing Campaigns"**
   - 🔗 Search "Mercari server driven UI marketing engineering blog"
   - How Mercari implemented SDUI specifically for time-limited campaigns — remote UI configuration with native performance.

10. **Zalando — "Evolving SDUI Framework for Scale"**
    - 🔗 Search "Zalando server driven UI framework"
    - European e-commerce giant's lessons on scaling SDUI to dozens of teams.

11. **Flipkart — Proteus (Their Own SDUI Engine)**
    - 🔗 https://proandroiddev.com/dynamic-screens-using-server-driven-ui-in-android-262f1e7875c1
    - Flipkart built *Proteus* — a drop-in replacement for Android's LayoutInflater that inflates JSON layouts at runtime. This is the Indian equivalent of Airbnb's Ghost Platform.
    - GitHub: https://github.com/flipkart-incubator/proteus

---

## Articles & Blog Posts

### Foundation Articles (Start Here)

| Article | Link | Why Read |
|---------|------|----------|
| **Understanding Client-Driven UI Limitations & Rise of SDUI** | https://medium.com/androidiots/understanding-client-driven-ui-limitations-and-the-rise-of-server-driven-ui-372a71c9c362 | Great conceptual intro — explains *why* SDUI, not just *what* |
| **Server-Driven UI Android Implementation** — Shubham Agrawal | https://medium.com/@iagrawalshubham/server-driven-ui-android-implementation-e4ae865b10d0 | Step-by-step Android implementation with code |
| **JetPack Compose With Server Driven UI** — Siva Ganesh | https://medium.com/android-dev-hacks/jetpack-compose-with-server-driven-ui-396a19f0a661 | Compose-specific SDUI patterns, reactive approach |
| **Server-Driven UI in Android with Compose (Part 1)** — Basalam | https://medium.com/basalam/server-driven-ui-in-android-with-compose-bf1885e9343c | Real-world multi-part series from a production team |
| **Understanding SDUI with Android and Jetpack Compose** — Dhiraj Thakur | https://medium.com/@dhirajkumar.dt51/understanding-server-driven-ui-with-android-and-jetpack-compose-ec1427b60ccd | Feb 2025, recent + practical with Firebase |
| **Android SDUI — XML vs Compose Benchmark** — İbrahim Ethem Şen | https://medium.com/@ibrahimethemsen/android-server-driven-ui-xml-vs-compose-example-benchmark-827a71d6605b | Side-by-side comparison + performance benchmarks |

### Intermediate / Architecture Deep Dives

| Article | Link | Why Read |
|---------|------|----------|
| **Server Driven UI — Concepts and Building Blocks** — Comviva | https://medium.com/@dfs.techblog/server-driven-ui-concept-db07d7946e94 | Strong conceptual foundation for the building blocks |
| **Server Driven UI for Mobile Apps** — Qantas Engineering | https://medium.com/qantas-engineering-blog/server-driven-ui-for-mobile-apps-48f8488ed7a4 | Pros/cons + backend design from an airline super app |
| **SDUI: The Necessary Evil for Scalable Mobile Apps** — Tushar Gupta | https://medium.com/digia-studio/server-driven-ui-sdui-the-necessary-evil-for-scalable-mobile-apps-80c650a2c8de | Excellent Dec 2025 article covering why every growth-stage company ends up here |
| **Server Driven UI** — RapiPay Engineering | https://medium.com/@tech.rapipay/server-driven-ui-80ae85603747 | Fintech perspective — strict data + UI separation |
| **Dynamic Screens Using SDUI in Android** — ProAndroidDev | https://proandroiddev.com/dynamic-screens-using-server-driven-ui-in-android-262f1e7875c1 | Covers Swiggy (Litho), Flipkart (Proteus), Airbnb (Epoxy) — Indian app ecosystem focus |
| **Design SDUI with Jetpack Compose and Firebase** — Stream/GetStream | https://getstream.io/blog/server-driven-compose-firebase/ | Deep technical blog post accompanying the skydoves repo. Covers layout nodes, action handlers, and versioning in detail. |
| **Case Study: Swiggy's Dynamic Widgets & SDUI** | https://medium.com/@viditsavaliya/cash-study-swiggys-dynamic-widgets-server-driven-ui-a-deep-dive-44adf0801c1d | Swiggy-specific deep dive with Jetpack Compose code snippets |
| **What Airbnb, Netflix, and Lyft Learned** | https://medium.com/@aubreyhaskett/server-driven-ui-what-airbnb-netflix-and-lyft-learned-building-dynamic-mobile-experiences-20e346265305 | Dec 2025 synthesis of all three companies' lessons |
| **Server Driven UI** — Dev.to | https://dev.to/nishant_keshav/server-driven-ui-3l0p | Good community-level explanation, beginner-friendly |

---

## YouTube Videos & Conference Talks

### 📹 Direct YouTube Videos

| Video | Channel | Why Watch |
|-------|---------|-----------|
| **How to Build Server Driven UI w/ Firebase + Jetpack Compose** | YouTube | 🔗 https://www.youtube.com/watch?v=tca-6yhWXNo — Hands-on tutorial, directly builds the system. Best for learning-by-coding alongside it. |
| **Server Driven UI with Jetpack Compose** | Curated Reality | 🔗 https://www.youtube.com/watch?v=rE9ZE0DzLFs — Compose-specific walkthrough |
| **A Page Out of Server Driven UI on Android** — Adit Lal | Droidcon | 🔗 https://www.youtube.com/watch?v=caX3GLXXGmw — Conference talk: emphasizes why SDUI is a hot topic and how to architect it |
| **Server Driven UI, Tom Lokhorst** | CocoaHeads | 🔗 https://www.youtube.com/watch?v=ERPmUsLkwEE — Real production implementation walkthrough |

### 🎙️ Conference Talks (Video + Transcript)

| Talk | Conference | Link |
|------|-----------|------|
| **Server-Driven UI for Mobile and Beyond** — Christopher Luu (Netflix) | QCon London 2024 | https://www.infoq.com/presentations/server-ui-mobile/ |
| **Server Driven UI — Streamlining Mobile Dev and Release** — Thomas Chao | QCon | https://www.infoq.com/presentations/sduie/ |
| **Dynamic Flow: Wise's KMP Approach to SDUI** | Droidcon 2024 | https://www.droidcon.com/2024/11/22/dynamic-flow-the-wise-approach-to-server-driven-ui/ |

### 🎬 Search These Terms on YouTube
- `"server driven UI" android jetpack compose`
- `"SDUI" android kotlin tutorial`
- `droidcon server driven UI`
- `"backend driven UI" android`
- `Flipkart Proteus Android`

---

## Documentation & Reference Sites

| Resource | Link | What's here |
|----------|------|-------------|
| **Jetpack Compose.app — SDUI Libraries** | https://www.jetpackcompose.app/Server-Driven-UI-libraries-in-Jetpack-Compose | Curated list of all SDUI libraries + code snippets for Jetpack Compose |
| **GitHub Topic: server-driven-ui** | https://github.com/topics/server-driven-ui | All public repos tagged with this topic, sorted by stars. Bookmark and check weekly. |
| **MobileNativeFoundation Discussions** | https://github.com/MobileNativeFoundation/discussions/discussions/47 | The best community discussion on SDUI strategies across companies and platforms |
| **Flipkart Proteus GitHub + Docs** | https://github.com/flipkart-incubator/proteus | Indian-built SDUI engine for Android. Well-documented with JSON schema examples. |
| **Beagle Framework Docs** | https://docs.usebeagle.io | Full SDUI framework by Zup IT — backend generates layout, Android/iOS/Web renders. Has getting started guide. |
| **Mobile Vitals — Android SDUI** | https://mobile-vitals.com/platform/android | Aggregates engineering blog posts from all major companies. Filter by "Server-Driven UI" |
| **InfoQ Mobile Track** | https://www.infoq.com/mobile/ | Regularly publishes SDUI case studies from QCon and other conferences |

---

## Podcasts

| Podcast | Episode | Link |
|---------|---------|------|
| **Lyft Mobile Podcast** | "Server Driven UI with Kevin Fang and Jeff Hurray" | Search Lyft Engineering podcast — discusses their Canvas SDUI system |
| **Android Developers Backstage** | Various Jetpack Compose episodes | https://adbackstage.libsyn.com/ |
| **Fragmented Podcast** | Episodes on modern Android architecture | https://fragmentedpodcast.com/ |

---

## Other Resources

### Tools & Libraries to Know

| Tool/Library | Purpose | Link |
|-------------|---------|------|
| **Proteus (Flipkart)** | Drop-in LayoutInflater replacement, inflates JSON at runtime | github.com/flipkart-incubator/proteus |
| **Litho (Meta)** | Declarative UI for complex Android views — Swiggy uses this | fblitho.com |
| **Epoxy (Airbnb)** | RecyclerView + SDUI for traditional Views | github.com/airbnb/epoxy |
| **Moshi** | JSON deserialization — better than Gson for sealed class polymorphism | github.com/square/moshi |
| **Kotlinx.serialization** | Official Kotlin JSON parser with sealed class support | kotlinlang.org/docs/serialization |
| **Beagle** | Full SDUI framework (backend + mobile) by Zup IT | docs.usebeagle.io |
| **Compose Multiplatform** | Take your SDUI renderer to iOS + Desktop | jetbrains.com/lp/compose-multiplatform |

### Communities

- **Android Dev Discord** — #architecture channel
- **Kotlin Slack** — #compose channel
- **r/androiddev** — search "SDUI" or "server driven"
- **ProAndroidDev** publication on Medium

---

## 🗺️ 12-Week Learning & Implementation Plan

> **Goal:** By Week 12, you will have built a working SDUI module in your **Aethera** e-commerce app and can confidently discuss it in interviews.

---

### Phase 1 — Foundation (Weeks 1–2)
*Understand the concept deeply before writing a single line.*

**Week 1 — The "Why"**
- [ ] Read: "Understanding Client-Driven UI Limitations & Rise of SDUI" (Medium/AndroIDIOTS)
- [ ] Read: Airbnb Ghost Platform blog post (the canonical paper)
- [ ] Read: Swiggy's Dynamic Widget blog post (because it's literally what you noticed)
- [ ] Read: Doist's "SDUI from a Mobile Perspective" (honest tradeoffs)
- [ ] Watch: "A Page Out of Server Driven UI on Android" — Adit Lal (Droidcon YouTube)
- **Deliverable:** Write 1 page of notes answering — "What problem does SDUI solve? When would I use it in Aethera?"

**Week 2 — The Architecture**
- [ ] Read: Q42's "One Code to Rule Them All: Android Server Driven UI"
- [ ] Read: "Server Driven UI — Concepts and Building Blocks" (Comviva)
- [ ] Study: MobileNativeFoundation Discussion #47 (at least the first 15 comments)
- [ ] Watch: QCon talk by Christopher Luu (Netflix) on InfoQ
- **Deliverable:** Draw your own diagram of the SDUI data flow for Aethera — from server JSON → Kotlin sealed class → Composable

---

### Phase 2 — First Implementation (Weeks 3–5)
*Get hands dirty with a real repo.*

**Week 3 — Clone & Explore**
- [ ] Clone `skydoves/server-driven-compose` — run it on your physical device
- [ ] Read the GetStream blog post alongside the repo code
- [ ] Map every component: Where is the JSON parsed? Where is `when(component)` written? Where are Composables called?
- [ ] Read the `server-driven-compose` data model files — understand the sealed class hierarchy

**Week 4 — Build Your First SDUI Screen**
- [ ] Create a new branch in `AetheraAdmin`: `feature/sdui-home-feed`
- [ ] Define your first 3 component types as sealed classes: `BannerCarousel`, `CategoryStrip`, `ProductRow`
- [ ] Write the JSON schema for each component (create mock JSON files)
- [ ] Write the Moshi/Kotlinx deserializer with polymorphism
- [ ] Write the `SduiRenderer` composable with `when(component)` dispatch

**Week 5 — Wire to Real Data**
- [ ] Create a mock API endpoint (can be a local JSON file served by Ktor or just hardcoded for now)
- [ ] Build the `SduiViewModel` with StateFlow + Loading/Success/Error states
- [ ] Handle the `Unknown` component type gracefully (no crash on unknown types)
- [ ] Add shimmer/skeleton loading while components load
- **Deliverable:** Working SDUI home feed with 3 component types rendering from JSON

---

### Phase 3 — Production Patterns (Weeks 6–8)
*Level up to real-world requirements.*

**Week 6 — Actions & Navigation**
- [ ] Design your action schema: `deeplink`, `navigate`, `api_call`, `bottom_sheet`
- [ ] Implement `SduiAction` sealed class
- [ ] Wire button taps → action handler → NavController / deep link router
- [ ] Study: How Lyft's Canvas handles action callbacks in protobuf
- [ ] Read: DoorDash "Facets" framework blog post

**Week 7 — Versioning & Backwards Compatibility**
- [ ] Study how `skydoves/server-driven-compose` handles versioning
- [ ] Implement a `minVersion` / `maxVersion` field on components
- [ ] Add logic: if app version < component's `minVersion`, skip component silently
- [ ] Read: Netflix's GraphQL backwards-compatibility strategy (from QCon talk)
- [ ] Implement: Server sends `app_version` as query param, backend responds with compatible component set

**Week 8 — Caching & Performance**
- [ ] Read: Swiggy's caching mechanism section in their blog post
- [ ] Implement: Cache last successful SDUI response in DataStore / Room
- [ ] Show cached UI instantly on app open → refresh in background (stale-while-revalidate pattern)
- [ ] Measure: Compare first-paint time with vs without caching using Android Profiler
- **Deliverable:** SDUI screen that loads from cache instantly and silently refreshes

---

### Phase 4 — Advanced & Showcase (Weeks 9–11)
*Build your flagship SDUI feature.*

**Week 9 — Theming & Design Tokens**
- [ ] Add color/style tokens to your JSON schema (`backgroundColor`, `textColor`, `cornerRadius`)
- [ ] Wire tokens to your Composables via `LocalCompositionLocal` or direct mapping
- [ ] Test: Change a component's color in JSON → verify it changes on device without app update
- [ ] Study: AirAsia's design token adoption blog post (Mobile Vitals aggregator)

**Week 10 — A/B Testing Simulation**
- [ ] Create two variants of your home feed JSON (Layout A: banner first, Layout B: categories first)
- [ ] Add a `user_segment` field to your API (based on user ID % 2)
- [ ] Server returns different component order based on segment
- [ ] Add analytics events to each component render (can be simple logs for now)
- [ ] Read: Shopify's "launch experiments whenever we deem necessary" blog post

**Week 11 — SDUI for Aethera Customer App**
- [ ] Apply all learnings to the *customer-facing* Aethera app (not just admin)
- [ ] Implement full SDUI home screen: banner carousel + category strip + product rows
- [ ] Write a 500-word technical README explaining your SDUI implementation — this goes on your portfolio
- [ ] Record a 3-minute screen recording demo for your portfolio website

---

### Phase 5 — Interview Readiness (Week 12)

**Week 12 — Consolidate & Tell the Story**

- [ ] Prepare 5 interview answers:
  1. "What is SDUI and why would you use it?" (2 min answer)
  2. "How would you implement SDUI in Jetpack Compose?" (3 min with code walkthrough)
  3. "How do you handle backwards compatibility in SDUI?" (2 min)
  4. "What are the tradeoffs of SDUI?" (2 min — be honest, show maturity)
  5. "Give me an example of a company that uses SDUI and how they do it." (name Swiggy/Zepto — your discovery story is a great hook)

- [ ] Add "Server-Driven UI" to your resume skills and AetheraAdmin project description:
  > "Implemented a Server-Driven UI module enabling the home feed layout and component order to be controlled server-side without app updates, using sealed classes, Moshi polymorphic deserialization, and Jetpack Compose rendering dispatch."

- [ ] Push the SDUI branch to your AetheraAdmin GitHub repo
- [ ] Add SDUI section to your portfolio website

---

### Quick Reference: Learning Order by Week

```
Week 1-2   → Read (Theory & Company Case Studies)
Week 3     → Explore (Clone & Study Real Code)
Week 4-5   → Build (First Working Implementation)
Week 6-7   → Level Up (Actions, Versioning)
Week 8     → Optimize (Caching, Performance)
Week 9-10  → Advanced (Theming, A/B Testing)
Week 11    → Ship (Portfolio-Ready Feature)
Week 12    → Interview Prep
```

---

### Starred Resources for Quick Revisit

| # | Resource | Type | Priority |
|---|---------|------|----------|
| 1 | Airbnb Ghost Platform Blog | Article | 🔴 Critical |
| 2 | skydoves/server-driven-compose | GitHub | 🔴 Critical |
| 3 | Swiggy Dynamic Widget Blog | Article | 🔴 Critical |
| 4 | GetStream SDUI + Firebase Blog | Article | 🟠 High |
| 5 | Q42 Android SDUI Engineering Blog | Article | 🟠 High |
| 6 | Netflix QCon 2024 Talk | Video/Transcript | 🟠 High |
| 7 | MobileNativeFoundation Discussion #47 | Community | 🟠 High |
| 8 | Flipkart Proteus GitHub | GitHub | 🟡 Medium |
| 9 | Doist SDUI Blog | Article | 🟡 Medium |
| 10 | Lyft Canvas Engineering Post | Article | 🟡 Medium |

---

*Happy building, Tarun. The fact that you noticed SDUI in production apps before studying it means you're already thinking like an engineer, not just a developer.*
