# 🪬 Milap — The Ancient Ritual, Reborn for The World

<div align="center">

**A blind matching ritual for the whole world**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-milap--eta.vercel.app-C9A84C?style=for-the-badge&logo=vercel&logoColor=white)](https://milap-eta.vercel.app)
[![Status](https://img.shields.io/badge/Status-Closed%20Beta-green?style=for-the-badge)](https://milap-eta.vercel.app)
[![Waitlist](https://img.shields.io/badge/Waitlist-2%2C400%2B-C9A84C?style=for-the-badge)](https://milap-eta.vercel.app)
[![Berlin](https://img.shields.io/badge/Berlin-2026-black?style=for-the-badge)](https://milap-eta.vercel.app)

</div>

> *Milap replaces mindless swiping with a sacred game — two compatible souls searching the same milk for one ring. No photos. No names. Just intention.*

---

## 📌 What is Milap?

Milap is a global dating app built around an ancient Indian wedding ritual — the **ring-in-milk ceremony** — where the bride and groom search together for a hidden ring. Whoever finds it first "wins." Milap translates this into a blind digital matching experience: two compatible users search a shared virtual pot simultaneously. When they find the same ring — it's a match.

No photos before matching. No names. No swiping. Just a daily 30-minute ritual at 9PM, powered by compatibility science and cultural soul.

**Closed Beta · Berlin 2026 · Solo Founded · Seed Stage**

---

## 🔴 The Problem — Dating Apps Are Broken

Modern dating apps have optimized for engagement, not connection:

| Pain Point | Reality |
|---|---|
| **Judged in 0.3 seconds** | Photos dominate decisions before any human quality is considered |
| **Infinite swiping** | Gamified for dopamine, not for depth |
| **Ghost culture** | No accountability, no ritual, no commitment signal |
| **Superficiality spiral** | The most attractive profiles win, not the most compatible people |

The data is clear: **despite billions of swipes, loneliness is rising.** Dating apps have become entertainment products, not connection products.

---

## 💡 Milap's Contrarian Approach

Milap makes three bets that go against every major dating app:

1. **Blind before beautiful** — Compatibility is calculated silently. You never see a photo before matching.
2. **Slow reveal over instant gratification** — Names on Day 3. Photos on Day 7. Commitment on Day 15.
3. **Daily ritual over infinite scroll** — The Kund opens once a day, for 30 minutes. Scarcity creates intention.

**Cultural angle:** The ring-in-milk ritual is recognized across South Asia and the Indian diaspora — but Milap is built for the whole world. The symbolism is universal: searching together, finding together, choosing together.

---

## 🔄 The Product — 4-Step Ritual Flow

```mermaid
flowchart LR
    A[🧮 Answer\n5 Questions] -->|Compatibility\nScore Calculated| B[🥛 Enter the Kund\n9PM · 30 min window]
    B -->|Search the milk\nfor your ring| C[💍 Ring Found!\nBlind Match]
    C -->|Progressive\nIdentity Reveal| D[🌹 Slow Reveal\nDay 3 → 7 → 15]

    style A fill:#1A0E08,stroke:#C9A84C,color:#F5ECD7
    style B fill:#1A0E08,stroke:#C9A84C,color:#F5ECD7
    style C fill:#1A0E08,stroke:#C9A84C,color:#F5ECD7
    style D fill:#1A0E08,stroke:#C9A84C,color:#F5ECD7
```

---

## 🌹 Progressive Reveal Timeline

```mermaid
timeline
    title Identity Reveal Journey
    Day 0  : Match confirmed
           : Anonymous chat begins
           : No name · No photo · Just words
    Day 3  : First name revealed
           : One word closer to a person
    Day 7  : Photo unveiled
           : See who you've been talking to
    Day 15 : Roka Option
           : Choose your path — partner or friend
```

---

## 🏗️ System Architecture

```mermaid
graph TB
    subgraph Client["📱 Client Layer"]
        RN[React Native\nExpo App]
        NX[Next.js\nMarketing Website]
    end

    subgraph Gateway["🔀 API Gateway"]
        GW[NestJS\nJWT Auth · Rate Limiting · CORS]
    end

    subgraph Services["⚙️ Core Services"]
        AUTH[Auth Service\nTwilio Verify OTP]
        MATCH[Matching Engine\nCompatibility · Kund Sessions]
        CHAT[Chat Service\nBlind Chat · Reveal Logic]
        PROFILE[Profile Service\nQuestionnaire · Scoring]
    end

    subgraph Realtime["⚡ Real-Time Layer"]
        WS[Socket.io\nWebSocket Gateway]
        BULL[BullMQ\nReveal Scheduler]
        REDIS[Redis · Upstash\nSession State · Pub/Sub]
    end

    subgraph Data["🗄️ Data Layer"]
        PG[PostgreSQL\nSupabase · Frankfurt]
        STORE[File Storage\nSupabase Storage]
    end

    RN -->|HTTPS + WebSocket| GW
    NX -->|Static + API| GW
    GW --> AUTH
    GW --> MATCH
    GW --> CHAT
    GW --> PROFILE
    MATCH <--> WS
    CHAT <--> WS
    WS <--> REDIS
    MATCH --> BULL
    BULL --> REDIS
    AUTH --> PG
    MATCH --> PG
    CHAT --> PG
    PROFILE --> PG
    PROFILE --> STORE
```

---

## 🛠️ Tech Stack — Reasoning Behind Each Choice

<div align="center">

![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-131415?style=for-the-badge&logo=railway&logoColor=white)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=for-the-badge&logo=twilio&logoColor=white)

</div>

| Technology | Role | Why This Choice |
|---|---|---|
| **NestJS** | Backend Framework | Modular architecture, TypeScript-first, decorator-based guards perfect for multi-service auth |
| **React Native + Expo** | Mobile App | Cross-platform with single codebase, EAS Build for Play Store submission, familiar React paradigm |
| **Next.js** | Marketing Website | SSR for SEO, App Router, Vercel deployment in one click |
| **PostgreSQL via Supabase** | Primary Database | Relational model fits the complex match/reveal/message relationships; Supabase adds RLS for privacy |
| **Prisma ORM** | Database Layer | Type-safe queries, migration management, schema-as-code |
| **Redis via Upstash** | Ephemeral State | Pot session state, real-time position tracking, rate limiting — needs sub-millisecond access |
| **Socket.io** | Real-Time Engine | Reliable WebSocket with fallback, room-based architecture perfect for shared Kund sessions |
| **BullMQ** | Job Scheduling | Delayed jobs for reveal timeline (Day 3, 7, 15) — reliable, Redis-backed |
| **Twilio Verify** | OTP Authentication | Phone-number-first auth, global coverage, no phone number storage needed |
| **TypeScript** | Type Safety | End-to-end type safety across backend and frontend reduces integration bugs |

---

## ⚙️ Core Engineering Decisions

### 1. Blind Matching Engine
The core constraint: **users must never be identifiable before a match.** This required designing the entire data model around anonymity:
- Pot sessions store only internal `userId` — no names, no photos in session state
- Ring positions are server-generated and stored in Redis per session
- Touch coordinates never reach the database — only match outcomes do
- Even post-match, profile data is gated by the reveal timeline state machine

### 2. Compatibility Scoring
Before entering the Kund, users answer 5 calibrated questions. Responses are converted into a vector and scored against other users using **cosine similarity**. Only pairs scoring above a defined threshold are pooled into the same Kund session. The magic feels serendipitous — the math is intentional.

The 5 questions target:
- Core values alignment
- Lifestyle compatibility  
- Communication style
- Long-term commitment orientation
- Social energy levels

### 3. Daily Window Implementation
The 9PM window is not just a product decision — it's an engineering constraint. A BullMQ cron job fires at 8PM to:
1. Create the day's `PotSession` record
2. Pre-compute the eligible user pool into Redis cache
3. Queue push notifications

At 9PM, compatible users are silently pooled. At 9:30PM, the session closes. Thundering herd mitigation: users are staggered by timezone (Mumbai 9PM → Berlin 9PM → New York 9PM).

### 4. Real-Time Ring Collision Detection
Both users' touch coordinates stream via WebSocket to a shared Redis-backed session. The server performs lightweight collision detection — if two users' coordinates land within a defined radius of the same ring within a 2-second window, a match event fires simultaneously to both clients via Redis pub/sub.

### 5. Privacy-First Architecture
- **Photos**: Stored in private Supabase Storage buckets. Never publicly accessible. Served only via time-limited signed URLs generated server-side — and only after the Day 7 reveal condition is met.
- **Phone numbers**: Verified via Twilio, never stored in plaintext in the application database.
- **Messages**: Encrypted at rest. The server never processes plaintext message content beyond delivery.
- **Block mechanism**: Silent vanish — the blocker's experience changes instantly; the blocked user receives no notification.

---

## 🔮 The Kund Matching Algorithm — Conceptual

```mermaid
sequenceDiagram
    participant UserA as User A (Mobile)
    participant Server as Matching Engine
    participant Redis as Redis Session
    participant UserB as User B (Mobile)

    UserA->>Server: join_session (sessionId)
    UserB->>Server: join_session (sessionId)
    Server->>Redis: Create shared pot room
    Server->>Redis: Place ring at random position (x, y)

    loop Every touch event
        UserA->>Server: update_position (x, y)
        Server->>Redis: Store User A coordinates
        Server->>Redis: Check collision with all other users
        Redis-->>Server: User B coordinates
        Server->>Server: Distance calculation
    end

    Note over Server: Distance < threshold AND within 2s window

    Server->>Redis: Claim ring, lock session
    Server->>UserA: match_found event
    Server->>UserB: match_found event
    Server->>Server: Create Match record + RevealTimeline
```

---

## 🎭 Progressive Identity Reveal — State Machine

```mermaid
stateDiagram-v2
    [*] --> Anonymous: Match Created
    Anonymous --> NameRevealed: Day 3 (BullMQ job fires)
    NameRevealed --> PhotoRevealed: Day 7 (BullMQ job fires)
    PhotoRevealed --> RokaAvailable: Day 15 (BullMQ job fires)
    RokaAvailable --> Committed: Both accept Roka
    RokaAvailable --> Friends: Choose friendship path
    Anonymous --> Blocked: Report & Vanish
    NameRevealed --> Blocked: Report & Vanish
    PhotoRevealed --> Blocked: Report & Vanish
```

Each state transition:
- Updates the `RevealTimeline` record in PostgreSQL
- Triggers a push notification to both users
- Changes what the API returns for `/profile/:matchId/reveal`
- The frontend reads reveal stage and renders accordingly — the backend enforces it, not the client

---

## 🎯 Product Design Decisions

### Why 30 Minutes?
Scarcity creates intention. A 30-minute daily window signals: *"This matters enough to show up for."* It also prevents the app from becoming a passive scroll — you either enter the Kund tonight, or you wait until tomorrow. This commitment signal self-selects for users who are serious.

### Why 9PM?
Behaviorally, evening is the highest-intention window for social connection. Post-work, pre-sleep — when people are most reflective and emotionally available. Culturally, evening rituals are deeply embedded in South Asian household rhythms. 9PM also creates a shared global moment — even across timezones, the *feeling* of "the Kund is open tonight" is synchronous.

### Why Slow Reveal?
The fastest path to disappointment in modern dating is photo-first judgment. Slow reveal forces conversation to carry the relationship for the first week. By the time photos are exchanged, both users have invested enough emotional capital that appearance becomes one factor — not the only factor. This is validated by decades of research on parasocial bonds and attachment formation.

### Why 5 Questions and Not 50?
Five questions answered honestly outperform fifty answered carelessly. The questionnaire is designed to be completed in under 3 minutes — low friction for high signal. Each question targets a distinct compatibility dimension. The cosine similarity model rewards alignment, not identity — two people can score high without being identical.

---

## 🚀 Deployment & Infrastructure

| Layer | Service | Reason |
|---|---|---|
| **Backend** | Railway | Zero-config NestJS deployment, GitHub CI/CD, environment variables UI |
| **Database** | Supabase (Frankfurt) | EU data residency, managed Postgres, built-in storage, RLS |
| **Cache/Queue** | Upstash Redis | Serverless Redis, no cold starts, pay-per-request at MVP scale |
| **Marketing Website** | Vercel | Next.js native, instant deploys, global CDN, custom domain |
| **Mobile** | Expo EAS | Managed build pipeline, OTA updates, Play Store submission |
| **SMS/OTP** | Twilio Verify | Global coverage, no phone number storage, compliant |

---

## 📊 Key Metrics & Status

| Metric | Value |
|---|---|
| Waitlist Signups | 2,400+ (pre-launch) |
| Beta Status | Closed Beta, Berlin 2026 |
| Founding Model | Solo Founded |
| Stage | Seed Stage |
| Mobile Platform | Android (Google Play — Closed Testing) |
| Backend Uptime | Railway managed |
| Website | [milap-eta.vercel.app](https://milap-eta.vercel.app) |

---

## 🧠 What I Learned Building Milap

**Solo founding a product with cultural soul is a different kind of hard.**

Most technical challenges have Stack Overflow answers. The hard problems in Milap were design problems disguised as technical ones:

- *How do you make anonymity feel magical, not eerie?* — Every UI decision, from blurred avatars to the "?" placeholder, had to communicate safety, not absence.
- *How do you build a real-time game that feels like a ritual?* — WebSocket latency and collision detection are engineering problems. Making them feel sacred is a design problem.
- *How do you build for slowness in a fast culture?* — Every product instinct says: give users more, faster. Milap's entire bet is the opposite. Resisting that instinct required constant conviction.

**On technical growth:** Building Milap end-to-end — from Prisma schema design to Socket.io collision detection to EAS build pipelines — forced a level of full-stack ownership that tutorials cannot replicate. Every architectural decision had a consequence I had to live with.

---

## 🗺️ Roadmap

```mermaid
gantt
    title Milap Launch Roadmap
    dateFormat  YYYY-MM
    section Beta
    Closed Beta Berlin          :done, 2026-04, 2026-06
    section Launch
    Android Public Launch       :2026-06, 2026-07
    iOS Launch                  :2026-07, 2026-09
    section Expansion
    Mumbai · Delhi · London     :2026-08, 2026-12
    Cultural ritual variations  :2026-10, 2027-02
    section Product
    Google OAuth                :2026-06, 2026-07
    Push Notifications          :2026-06, 2026-07
    Diya Streak System          :2026-07, 2026-08
    Shared Playlist Ritual      :2026-08, 2026-09
```

---

## ✍️ Founder Note

> *"I built Milap to prove that Indian symbolism can meet global product craft — not as nostalgia, but as a new interface for intention. Dating apps taught us to judge fast. Milap asks you to wait, to search, to find — together. That patience is the product."*
>
> — **Saurabh Kumar**, Founder & CEO

**Saurabh Kumar**
Founder & CEO, Milap
MSc Artificial Intelligence, BSBI Berlin
B.Tech, CUSAT Kerala
Ex-Technical Head @ Pashi Technology · Full Stack Developer · Data Analyst
Previously built **Vocaa** — a language learning platform

*Milap is a solo-founded startup built with code, culture, and conviction.*

---

## 📬 Contact & Links

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-saurabhmauryaa.com-C9A84C?style=for-the-badge&logo=safari&logoColor=white)](https://saurabhmauryaa.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/saurabhkumar)
[![Email](https://img.shields.io/badge/Email-saurabhkumar9493%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:saurabhkumar9493@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-saurabhkumar5-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/saurabhkumar5)

**📍 Berlin, Germany · Open to Werkstudent & Full-Stack Engineer roles**

</div>

---

<div align="center">

*© 2026 Milap · Made with 🪬 in Berlin, Germany*
*Solo founded · Seed stage · The Kund opens at 9PM*

</div>
