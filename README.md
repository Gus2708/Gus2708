# Hi there, I'm Gustavo Reyes 👋

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&pause=1000&color=2F80ED&center=true&vCenter=true&width=700&lines=Full+Stack+Developer+(Python+%C2%B7+React);LLM%2C+RAG+%26+AI+Agents+in+Production;Software+real+businesses+use+every+day" alt="Typing SVG" />
</div>

---

### 🚀 About Me

Full Stack Developer who ships **AI into production**, not into demos. Four of the projects below run every day at real businesses — an autonomous WhatsApp agent that serves live customers, an analytics app, a mobile POS, and a humanitarian real-time feed.

I measure what I ship. The retrieval pipeline behind my WhatsApp agent is benchmarked against **320 real customer queries** (76.9% exact recall, 6.3% failure rate), and I redesigned the embedding input to lift the vector layer's signal-to-noise **10x**.

Coming from an Operations Management background (where I led a team of 7 and cut inventory discrepancies by ~30%), I approach engineering problem-first: I've seen the bottlenecks from the inside and built the software to fix them.

- 🌍 **Based in:** Venezuela · **Available for 100% Remote Roles**
- 🗣️ **Languages:** Spanish (Native) · English (B2 – Upper Intermediate)
- 🧠 **Focus:** RAG & Vector Search · AI Agents & Tool Calling · LLM Evaluation · Full-Stack SaaS · React Native
- 📫 **Reach me at:** gusreyes_dev@outlook.com · [LinkedIn](https://www.linkedin.com/in/gusreyes-dev/)

---

### 💻 Tech Stack & Tools

**AI & Retrieval**  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-6566F1?style=for-the-badge&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)

**Frontend & Mobile**  
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)

**Backend & Data**  
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-181818?style=for-the-badge&logo=supabase&logoColor=3ECF8E)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

**Engineering Practice**  
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![TDD](https://img.shields.io/badge/TDD_%2F_Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)

---

### 🏆 Featured Projects

*Software in real production use, with a focus on AI integration, secure data access, and measured results.*

#### 1. [WhatsApp AI Agent — "Perucho"](https://github.com/Gus2708/whatsapp-agent) — Autonomous Customer Service & Quoting Assistant · *In production*
An event-driven WhatsApp agent serving real customers daily at Ferretería El Serrucho: answers inventory questions, generates exact quotes from live POS pricing, transcribes voice notes, and escalates to staff when a human is needed.
* **Tech:** n8n · WAHA · OpenAI (via OpenRouter) · `text-embedding-3-small` + pgvector · Groq Whisper · Supabase · PostgreSQL · Docker.
* **Highlights:** **5-layer retrieval pipeline** over a 7,000+ SKU catalog (lexical & measurement parsing → 3.5k-term catalog dictionary → `pg_trgm` fuzzy matching → vector search → LLM semantic rescue), resolving the common query in **~900 ms at zero marginal cost**.
* **Measured:** benchmarked on **320 real customer queries** — **76.9% exact recall, 6.3% failure rate**. Redesigning the embedding input (description + category + colloquialisms) lifted the vector layer's signal-to-noise **10x**, adding **+7 correct matches** over lexical-only retrieval.
* **Production guards:** read-only DB connection for safe pricing · LLM output sanitization · rate limiting · CI sync tests.

#### 2. [El Serrucho GO](https://github.com/Gus2708/el-serrucho-go) — Real-Time Inventory & Sales Analytics · *In production* · [Live demo](https://el-serrucho-go.vercel.app)
A mobile + PWA analytics dashboard in daily use at the store, shipped as an Android app (EAS) and an installable PWA from a single codebase via `react-native-web`.
* **Tech:** Expo · React Native · TypeScript · Supabase · PostgreSQL · Python · Google Gemini.
* **Highlights:** closed-loop writeback engine bridging an on-premise POS to the cloud through a Python watchdog · Gemini anomaly detection in Supabase Edge Functions · RLS role-approval gates · the staff queue that resolves the AI agent's escalations · virtualized inventory list.

#### 3. [CaobaPOS](https://github.com/Gus2708/CaobaPos) — Mobile Point-of-Sale & Inventory System · *Client project, in production* · [Live demo](https://caoba-pos.vercel.app)
A tablet-first cross-platform POS actively used by a paying café client, built for small businesses with unstable internet.
* **Tech:** React Native · Expo (SDK 54) · TypeScript · Supabase · PostgreSQL.
* **Highlights:** offline-first inventory · real-time sync · multi-tenant access via Row Level Security · barcode scanning · branded PDF invoices · date-range financial dashboards with transaction cancellation and automatic stock restoration.

#### 4. [Venezuela Earthquake Feed](https://github.com/Techeasy-Latam/vzla-sismo-feed) — Real-Time Verified Humanitarian Feed · *Open source · 6 ★* · [Live demo](https://vzla-sismo-feed.vercel.app)
A verified real-time information feed built with the Techeasy LATAM community during the Venezuela earthquake, to counter misinformation when it mattered most. **73 commits contributed.**
* **Tech:** Next.js · TypeScript · Supabase · Claude API · PWA.
* **Highlights:** AI-assisted verification of incoming reports · installable PWA for low-connectivity conditions · built and shipped under real time pressure with a distributed team.

#### 5. [Splitty](https://github.com/4GeeksAcademy/splitty-kmjg) — AI-Powered Expense Splitting Platform · *Final Capstone, 4Geeks Academy* · [Live demo](https://splitty-kmjg.vercel.app/)
A full-stack FinTech app that removes the friction of group expenses through AI data extraction and optimized settlements.
* **Tech:** React 18 · Flask · PostgreSQL · Supabase · Google Gemini · PayPal · Vercel · Render.
* **Highlights:** heap-based settlement algorithm that **cuts inter-party transactions by up to 50%** · Gemini-powered receipt parsing · 30+ RESTful endpoints with JWT lifecycle, bcrypt and rate limiting · dual-cloud deploy via GitHub CI/CD.

---

### 📈 GitHub Analytics

<div align="center">

[![Gustavo's GitHub Stats](https://github-readme-stats-henna-one-70.vercel.app/api?username=Gus2708&count_private=true&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117)](https://github.com/Gus2708)

[![Top Languages](https://github-readme-stats-henna-one-70.vercel.app/api/top-langs/?username=Gus2708&count_private=true&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117)](https://github.com/Gus2708)

</div>
