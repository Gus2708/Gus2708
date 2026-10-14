# Hi there, I'm Gustavo Reyes 👋

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&pause=1000&color=2F80ED&center=true&vCenter=true&width=700&lines=Full+Stack+Developer+(Python+%C2%B7+TypeScript);RAG%2C+Vector+Search+%26+Evaluations+in+Production;5+Production+Repos+with+Passing+CI" alt="Typing SVG" />
</div>

---

### 🚀 About Me

Full Stack Developer with an Operations Management background (led retail store operations with a team of 7 and cut inventory discrepancies by ~30%). I build software to solve the operational bottlenecks I experienced first-hand, with production systems running daily for paying businesses.

- 🌐 **Portfolio:** [gusdev.me](https://gusdev.me)
- 🧠 **Focus:** Multi-Stage RAG Pipelines · Production AI Agents · Deterministic Evaluations · Offline-First Architectures · Hybrid Cloud Sync
- 🌍 **Location:** Venezuela · Available for 100% Remote Roles
- 🗣️ **Languages:** Spanish (Native) · English (B2 certified, C1 Reading/Writing)
- 📫 **Contact:** [LinkedIn](https://www.linkedin.com/in/gustavo-reyes-dev) · gusreyes_dev@outlook.com

---

### 💻 Stack & Verified Tooling

- **AI, RAG & Search:** OpenAI API, OpenRouter, Google Gemini, `pgvector`, `pg_trgm`, Groq Whisper, n8n, automated retrieval ablation suites.
- **Languages & Frameworks:** TypeScript, Python, JavaScript, SQL, React 18, React Native (Expo SDK 54), Next.js, Flask.
- **Databases & Cloud:** PostgreSQL, Supabase (Auth, Row Level Security, Edge Functions, Realtime), Docker.
- **Testing & Continuous Integration:** Pytest, Jest, GitHub Actions CI matrices, TDD.

---

### 🛠️ Featured Systems & Engineering Case Studies

#### 1. <img src="https://github.com/user-attachments/assets/ac3c26e3-547b-4787-8965-9bd38d86013a" width="24" height="24" style="vertical-align: middle; border-radius: 4px;" /> [WhatsApp AI Agent - "Perucho"](https://github.com/Gus2708/whatsapp-agent) · *In production at Ferretería El Serrucho*
Autonomous customer service and quoting assistant serving live retail customers over a 7,000+ SKU hardware store catalog.
* **5-Layer Retrieval Architecture:** Fast lexical & measurement parser (`parser_medidas.js`) → 3,500-term catalog dictionary → PostgreSQL `pg_trgm` fuzzy matching → vector similarity via Supabase `pgvector` (`text-embedding-3-small`) → LLM fallback via OpenRouter.
* **Performance & Cost:** Resolves high-frequency queries in ~900 ms on the zero-marginal-cost lexical layer before invoking LLM inference.
* **Deterministic Evaluation:** Benchmarked against 320 synthetic colloquial customer queries (`scripts/_test_coloquial.js`), scoring 76.9% exact recall and 6.3% failure rate. Redesigned compound embedding strings (title + category + local synonyms) lifted vector signal-to-noise 10x over raw text.
* **Operational Impact:** Human escalation requests dropped from 46 historical cases to 2 in the last 10 days, with 61% of escalations filtered as non-retrieval operational inquiries.
* **Safety & Guardrails:** Enforces read-only database connections for pricing, prompt injection sanitization, rate limiting, and automated CI sync tests.

<details>
  <summary>📸 <b>View Flight Deck Interface</b></summary>
  <br />
  <p align="center">
    <img src="https://github.com/user-attachments/assets/1597cb5b-3091-45fe-8e84-21f49a11c19f" alt="Flight Deck Live Preview" width="800" style="border-radius: 8px;" />
  </p>
</details>

#### 2. <img src="https://github.com/user-attachments/assets/148272ad-d174-47fe-8ea9-056fe11740d7" width="24" height="24" style="vertical-align: middle; border-radius: 4px;" /> [El Serrucho GO](https://github.com/Gus2708/el-serrucho-go) · *In production* · [Live app](https://el-serrucho-go.vercel.app)
Store operations management, inventory tracking, and field ordering platform delivered as an Android app (EAS) and an installable PWA from a single codebase via `react-native-web`.
* **Scale & Test Suite:** 34,800+ lines of TypeScript across 130+ files, backed by 61 Jest unit and integration tests across 10 suites in GitHub Actions CI.
* **Architecture:** Closed-loop writeback system linking local POS hardware to the cloud via a Python watchdog process. Implements dual-currency order settlement (USD and bolívares with markup calculation) and eliminates race conditions between order emission and item persistence.
* **Cloud & Security:** Supabase Edge Functions with Gemini anomaly detection, Row Level Security permission gates, and a staff resolution queue for WhatsApp bot escalations.

<details>
  <summary>📸 <b>View Mobile Interface Mockup</b></summary>
  <br />
  <p align="center">
    <img src="https://github.com/user-attachments/assets/b9ed518a-0443-4253-8685-307c5911c090" alt="El Serrucho GO Mockup Interface" width="800" style="border-radius: 8px;" />
  </p>
</details>

#### 3. <img src="https://github.com/user-attachments/assets/3f9e2a55-e9e6-4858-a101-8b42575fe68e" width="24" height="24" style="vertical-align: middle; border-radius: 4px;" /> [CaobaPOS](https://github.com/Gus2708/CaobaPos) · *Client project in production* · [Live app](https://caoba-pos.vercel.app)
Tablet-first cross-platform POS and inventory system actively operated by a commercial café client in an environment with unstable internet connectivity.
* **Quality & CI:** 100 Jest tests across 19 test suites verified on every commit in GitHub Actions CI.
* **Offline-First Resilience:** Optimistic local state management with background reconciliation to Supabase PostgreSQL, barcode scanning, thermal receipt and branded PDF generation.
* **Business Logic:** Date-range financial reporting, role-based authorization via PostgreSQL RLS, and transaction cancellation with automatic stock restoration.

<details>
  <summary>📸 <b>View Tablet Interface</b></summary>
  <br />
  <p align="center">
    <img src="https://github.com/user-attachments/assets/7ec0c305-bb6f-4235-b339-82491628c99c" alt="Caoba POS Tablet Interface" width="800" style="border-radius: 8px;" />
  </p>
</details>

#### 4. [Hybrid-on-Cloud](https://github.com/Gus2708/Hybrid-on-cloud) · *Enterprise synchronization bridge*
Real-time bridge connecting an on-premise Windows desktop POS system (`.dat` files) to Supabase cloud infrastructure.
* **Verification:** 140 pytest unit and integration tests running on `windows-latest` via GitHub Actions CI.
* **Core Capabilities:** Bidirectional price updating (`batch_price_updater`), transactional data integrity checks, multi-source entity reconciliation, and change-data capture.

#### 5. [Retrieval Ablation CLI](https://github.com/Gus2708/retrieval-ablation) · *Open source research tooling*
Command-line benchmarking suite designed to perform automated layer-by-layer ablation studies on multi-stage search and RAG architectures.
* **Functionality:** Isolates lexical, trigram, dense vector, and LLM re-ranking layers to measure marginal recall gains, latency overhead, and token cost per stage.

#### 6. [Venezuela Earthquake Feed](https://github.com/Techeasy-Latam/vzla-sismo-feed) · *Open source humanitarian initiative · 6 ⭐* · [Live app](https://vzla-sismo-feed.vercel.app)
Real-time verified information platform built during the Venezuela earthquake to counteract crisis misinformation.
* **Contributions:** 73 commits contributed to core development. Built with Next.js, Supabase, and Claude API for report verification, optimized as an offline-ready PWA for low-connectivity emergencies.

---

### 📊 GitHub Activity

<div align="center">

[![Gustavo's GitHub Stats](https://github-readme-stats-henna-one-70.vercel.app/api?username=Gus2708&count_private=true&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117)](https://github.com/Gus2708)

[![Top Languages](https://github-readme-stats-henna-one-70.vercel.app/api/top-langs/?username=Gus2708&count_private=true&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117)](https://github.com/Gus2708)

</div>
