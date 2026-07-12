<!-- ================= HEADER ================= -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Yash%20Aggarwal&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Building%20AI%20systems%20for%20people%20who%20need%20them%20most&descAlignY=55&descSize=18" width="100%"/>

<a href="https://github.com/yash4428">
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&duration=3000&pause=800&color=58A6FF&center=true&vCenter=true&width=650&lines=AWS+AIdeas+2026+Global+Champion+%F0%9F%8F%86;ML+%2B+Full-Stack+%2B+Systems;Computer+Engineering+%40+TIET+(9.67+CGPA);Ship+for+users+the+industry+forgets" alt="Typing SVG" />
</a>

<br/><br/>

<img src="https://img.shields.io/badge/%F0%9F%8F%86_AWS_AIdeas_2026-GLOBAL_CHAMPION-FF9900?style=for-the-badge&labelColor=232F3E"/>
<img src="https://img.shields.io/badge/Open_to-SWE_Internships-2ea44f?style=for-the-badge"/>
<img src="https://komarev.com/ghpvc/?username=yash4428&style=for-the-badge&color=58A6FF&label=PROFILE+VIEWS"/>

<br/><br/>

<a href="https://www.linkedin.com/in/yash-aggarwal-cs/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://leetcode.com/u/yash4428/"><img src="https://img.shields.io/badge/LeetCode_270%2B-FFA116?style=for-the-badge&logo=leetcode&logoColor=black"/></a>
<a href="https://portfolio-wheat-xi-79.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white"/></a>
<a href="mailto:yashaggarwal1029@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>

</div>

---

## 👋 About me

Computer Engineering undergrad at **Thapar Institute of Engineering & Technology** (2024–2028, CGPA **9.67/10**). First-generation engineer who learned cloud and ML through hackathons, free tiers, and AWS credits.

My pattern: **AI for underserved users.** Parkinson's screening over voice, smartphone guidance for the elderly, offline emergency response for zero-connectivity zones, financial literacy over WhatsApp for rural India. If the "default user" gets ignored by tech, that is who I build for.

- 🏆 **AWS AIdeas 2026 Global Champion** with CogniSense
- 🥈 Runner-Up at **HackTU 7.0** · 🥇 Winner at **NIT Delhi Codeslayers**
- 🧩 **270+ LeetCode** problems solved
- 🔭 Currently building: **Sahayak** — macOS AI guidance app with a multi-layer screen-understanding pipeline

---

## 🛠️ Tech stack

<div align="center">

**Languages**

<img src="https://skillicons.dev/icons?i=cpp,python,swift,ts,js,kotlin&theme=dark"/>

**ML / AI**

<img src="https://skillicons.dev/icons?i=pytorch,sklearn,tensorflow&theme=dark"/>
<img src="https://img.shields.io/badge/AWS_Bedrock-Nova_%7C_Titan-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white"/>
<img src="https://img.shields.io/badge/YOLO-Computer_Vision-00FFFF?style=flat-square"/>
<img src="https://img.shields.io/badge/RAG-Vector_Search-8A2BE2?style=flat-square"/>

**Backend & Cloud**

<img src="https://skillicons.dev/icons?i=nodejs,express,fastapi,aws,postgres,supabase,vercel&theme=dark"/>

**Frontend & Mobile**

<img src="https://skillicons.dev/icons?i=react,nextjs,threejs,apple,androidstudio&theme=dark"/>

</div>

---

## 🚀 Flagship projects

### 🏆 CogniSense — ML-based Parkinson's Screening · *AWS AIdeas 2026 Global Champion*

> Screening pipeline using voice, facial, and motor signals — delivered over WhatsApp so it works on any phone.

- **85% ROC-AUC** on clinical Parkinson's risk classification, **<500ms** inference latency
- 30+ acoustic features (jitter, shimmer, HNR, MFCC), benchmarked across SVM, Random Forest, and Gradient Boosting
- Live demo shipped to international judges; selected champion from a global pool

`Python` `scikit-learn` `Signal Processing` `AWS Bedrock` `REST APIs`

🔗 [github.com/Cogni-sense1](https://github.com/Cogni-sense1)

<details>
<summary><b>🧠 How the ML pipeline works (click to expand)</b></summary>
<br/>

```mermaid
flowchart LR
    A[Voice sample] --> B[Noise filtering]
    B --> C[Segmentation]
    C --> D[Feature extraction<br/>jitter · shimmer · HNR · MFCC]
    D --> E{Model ensemble<br/>SVM · RF · GBM}
    E --> F[Risk score<br/>85% ROC-AUC]
    F --> G[WhatsApp delivery<br/>under 500ms]
```

</details>

---

### 🖥️ Sahayak — macOS AI Guidance for Non-Technical Users

> Menu bar app that walks elderly and non-technical users through any software task with a pulsing on-screen overlay plus voice instructions.

- Multi-layer screen detection: Accessibility Tree (**5ms**) to Apple Vision OCR (**40ms**) to dual YOLO in parallel to Nova 2 Lite fallback (**800ms**)
- Semantic plan cache with **pgvector** (0.92 similarity threshold) to cut redundant LLM calls
- Successor to **Waylo** (Android), which used a three-tier detection pipeline with a failure-logging flywheel for continuous YOLO retraining

`Swift` `SwiftUI` `AppKit` `Node.js` `FastAPI` `AWS Bedrock` `Aurora PostgreSQL + pgvector`

🔗 Waylo: [github.com/waylo-1](https://github.com/waylo-1)

<details>
<summary><b>⚡ The detection cascade (click to expand)</b></summary>
<br/>

```mermaid
flowchart TD
    Q[User asks: how do I send an email?] --> L0[L0 · Accessibility Tree · 5ms]
    L0 -->|miss| L1[L1 · Apple Vision OCR · 40ms]
    L1 -->|miss| L25[L2.5 · Dual YOLO in parallel<br/>OmniParser + Screen2AX]
    L25 -->|miss| L3[L3 · Nova 2 Lite vision · 800ms]
    L0 --> O[Pulsing overlay + voice instruction]
    L1 --> O
    L25 --> O
    L3 --> O
    C[(pgvector plan cache<br/>0.92 threshold)] -.->|cache hit skips LLM| O
```

Cheapest layer first. The LLM is the last resort, not the first call.

</details>

---

### 📊 Amex Campus Challenge 2026 — Unsupervised Profitability Ranking

> Rank 500k cardmembers by profitability with **no ground-truth labels**, scored on top-20% overlap.

- Best public leaderboard score: **0.919**
- Method: economic P&L modeling, probe-based submissions, formula inversion, set reconstruction, proportion-supervised GBM
- Key insight: diverse consensus rankings beat concentrated approaches

`Python` `EDA` `Gradient Boosting` `Feature Engineering`

---

### 🧍 Rehabify — Gamified CV Physiotherapy

> Real-time pose estimation that turns physio exercises into a guided, gamified feedback loop.

- **90%+** motion detection accuracy tracking 33 body landmarks with joint-angle computation and automated rep-counting
- Full-stack: React frontend, Node.js backend, ML inference over REST APIs

`Python` `MediaPipe` `React` `Node.js`

🔗 [github.com/Rehabify-GamifiedPhysiotherapy](https://github.com/Rehabify-GamifiedPhysiotherapy)

---

### 🆘 ResQAI — Offline-First Emergency Response PWA

> Emergency guidance that works with **zero internet**, built for rural and low-connectivity environments.

- Locally hosted Gemma LLM (Ollama) with RAG over WHO and Red Cross protocols using local vector embeddings, covering 9 incident types
- Severity triage engine (Critical / High / Moderate / Low) plus multilingual voice I/O in Hindi, Punjabi, and English

`React` `TypeScript` `PWA` `Gemma / Ollama` `RAG` `IndexedDB`

🔗 [github.com/ResQAI1](https://github.com/ResQAI1)

---

### 💸 Financio — Financial Literacy over WhatsApp

> NLP-driven financial learning for rural users, with no app install needed.

- **35% reduction** in concept learning time across test users
- Node.js/Express and MongoDB backend serving personalized simulations through WhatsApp

`Node.js` `Express` `MongoDB` `WhatsApp API` `NLP`

🔗 [github.com/FinanciomitraAi](https://github.com/FinanciomitraAi)

---

<details>
<summary><b>🌏 More builds (click to expand)</b></summary>
<br/>

**ClimateWatch India — ISRO Hackathon** · Hyperlocal monsoon-failure predictor with an animated climate time-machine. `Python/xarray` `ConvLSTM (PyTorch)` `FastAPI` `React + Deck.gl/Mapbox` `D3.js`

**CommunityOS (CrisisLens)** · 🔗 [github.com/communityos-crisislens](https://github.com/communityos-crisislens)

**3D Portfolio** · Scroll-driven site with a particle-field hero and skill constellation. `Three.js` `React Three Fiber` `GSAP` `Next.js 14` · 🔗 [Live site](https://portfolio-wheat-xi-79.vercel.app/)

</details>

---

## 📈 GitHub stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=yash4428&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&count_private=true" height="170"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yash4428&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117" height="170"/>

<img src="https://streak-stats.demolab.com?user=yash4428&theme=tokyonight&hide_border=true&background=0d1117"/>

<img src="https://raw.githubusercontent.com/yash4428/yash4428/output/github-contribution-grid-snake-dark.svg" alt="snake animation"/>

</div>

---

## 🏅 Achievements

| | |
|---|---|
| 🏆 | **AWS AIdeas 2026 Global Champion** — CogniSense, international panel-judged competition |
| 🥈 | **Runner-Up, HackTU 7.0** |
| 🥇 | **Winner, Codeslayers Hackathon**, NIT Delhi |
| 📊 | **0.919** best public score, Amex Campus Challenge 2026 |
| 🧩 | **270+** LeetCode problems (DP, graphs, Dijkstra, Kosaraju SCC, Rabin-Karp) |
| 🎓 | **9.67/10 CGPA** at TIET · ML Specialization (DeepLearning.AI x Stanford, all 3 courses) |

---

## 🤝 Beyond code

Technical Member — **Saturnalia Tech Fest** · **MarkFin Society** · **Echoes Media Club** @ TIET

---

<div align="center">

### 💬 If you are building something for users the industry forgot, let us talk.

<a href="mailto:yashaggarwal1029@gmail.com"><img src="https://img.shields.io/badge/yashaggarwal1029@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/yash-aggarwal-cs/"><img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=120&section=footer" width="100%"/>

</div>
