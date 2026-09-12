<div align="center">
  <img height="140" src="https://avatars.githubusercontent.com/u/91460490?v=4" alt="John Apollo Ponteras" style="border-radius: 50%;" />
  <h1>John Apollo Ponteras</h1>
  <p><strong>Full-Stack Developer | Backend & Cloud Infrastructure | BSCpE (Cum Laude)</strong></p>
  <p>Las Piñas, Philippines</p>

  <p>
    <a href="https://www.linkedin.com/in/john-apollo-ponteras-478036213" target="_blank">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" height="32" alt="LinkedIn" title="LinkedIn" />
    </a>
    &nbsp;&nbsp;
    <a href="mailto:japollop.we@gmail.com">
      <img src="https://cdn.simpleicons.org/gmail/EA4335" height="32" alt="Email" title="Email" />
    </a>
    &nbsp;&nbsp;
    <a href="https://dev.to/apollo-jhn" target="_blank">
      <img src="https://cdn.simpleicons.org/devdotto/0A0A0A/FFFFFF" height="32" alt="Dev.to" title="Dev.to: apollo-jhn" />
    </a>
    &nbsp;&nbsp;
    <a href="https://discord.com/users/apollocube" target="_blank">
      <img src="https://cdn.simpleicons.org/discord/5865F2" height="32" alt="Discord (apollocube)" title="Discord: apollocube" />
    </a>
    &nbsp;&nbsp;
    <a href="https://www.youtube.com/channel/UCavnsSQiD-lv5fszwUaUuYw" target="_blank">
      <img src="https://cdn.simpleicons.org/youtube/FF0000" height="32" alt="YouTube" title="YouTube" />
    </a>
  </p>

  <p>
    <img src="https://visitor-badge.laobi.icu/badge?page_id=apollo-jhn.apollo-jhn&" alt="Profile Visitors" />
  </p>
</div>

---

### 👨‍💻 About Me

Hi there! 👋 I am John Apollo Ponteras, a Full-Stack Developer from the Philippines. I graduated **Cum Laude** with a Bachelor of Science in Computer Engineering.

I build secure backend services, modern web platforms, and cloud infrastructure. Most of my daily work involves Python (Django, DRF, Celery, Channels), modern JavaScript and TypeScript (Next.js, React), and cloud platforms on Microsoft Azure and DigitalOcean.

Because of my Computer Engineering training, I look at software with a systems-level perspective. I care about database efficiency, memory usage, network reliability, and clean architecture from low-level microcontrollers up to distributed cloud services.

* 💡 **Philosophy:** If I can envision it, I can build it. I enjoy turning complex requirements into fast, working software that people can rely on.
* 🔭 **Current Work:** Backend Developer at **Everion Platforms (Flair)**, building real-time APIs, WebSockets, and payment integrations.
* 🏛️ **Past Leadership:** Former Information Officer I and Tech Lead in the **Office of the President - Climate Change Commission**, delivering public national web platforms and managing cloud infrastructure.
* 🛡️ **Quality & Security:** Strong focus on automated testing (achieved ~99.5% test coverage across core apps) and application security (Fernet PII encryption at rest, custom device-fingerprint JWT auth, and SSL-secured database pools).
* 🤖 **AI & Systems:** Experienced with AI-assisted engineering (Claude Code, Antigravity) and building LLM context-management systems (memory scratchpads, tokenizers, and SQLite persistence).
* 💬 **Ask Me About:** Python, Django, Next.js, Redis, PostgreSQL schema design, and asynchronous systems.
* 📫 **Contact:** Reach me at **japollop.we@gmail.com** or connect with me on **[LinkedIn](https://www.linkedin.com/in/john-apollo-ponteras-478036213)**.

---

### 🏛️ Architectural Case Studies

Here are three engineering challenges from my production work and how I solved them:

#### 1. High-Traffic Database Scaling and Lock Mitigation (EcoSaver)
* **Challenge:** During high public traffic spikes, MySQL suffered from connection pool exhaustion and lock wait timeouts (`Lock wait timeout exceeded`) caused by multiple concurrent requests trying to update the same visit counter rows.
* **Architecture & Solution:** I designed an append-only delta table buffered through Redis. Instead of running locking updates on primary database rows on every page view, incoming visits are recorded in Redis and written in asynchronous batches. This eliminated row lock contention and preserved fast response times under heavy load.

#### 2. Private Media Storage Seam (Flair)
* **Challenge:** User portfolios, applicant documents, and dispute evidence needed strong access control. Files could not be stored in public CDN buckets or indexed by search engines, but still had to stream quickly for authorized users.
* **Architecture & Solution:** I architected a private storage seam using auth-gated streaming endpoints backed by non-CDN S3/Spaces buckets. I used `LazyObject` storage proxies so the application verifies authentication, permissions, and active subscriptions before serving any protected media.

#### 3. Real-Time WebSocket Infrastructure with State Reconciliation (Flair)
* **Challenge:** Real-time chat needed to support multiple participants, mobile reconnection, message delivery confirmation, and reliable message ordering without race conditions.
* **Architecture & Solution:** I implemented WebSocket consumers with Django Channels, Daphne, and Redis. The system includes message-ID reconciliation, read-receipt watermarks, participant mute states, and strict `(created_at, public_id)` cursor pagination tiebreakers to prevent duplicate or skipped messages during network handoffs.

---

### 🚀 Featured Open Source Repositories

These are open source tools and systems I built and maintain on GitHub:

* **[compact-chat-engine](https://github.com/apollo-jhn/compact-chat-engine)** `Python` `SQLite` `Rich CLI` `pytest`  
  A terminal chat tool for OpenAI-compatible APIs that prevents context window overflow. It automatically synthesizes older conversation history into a structured memory scratchpad, features a tiered token counting system (Hugging Face, tiktoken, heuristic), and includes full test coverage with pytest.

* **[SWAVE-DesignProject](https://github.com/apollo-jhn/SWAVE-DesignProject)** `Python` `Flask` `React` `Raspberry Pi`  
  Smart Water Vending Machine capstone project. As lead programmer, I built the multi-threaded edge controller handling pump relays, interrupt-driven coin acceptors, ultrasonic volume sensors, and a touchscreen user interface.

* **[windows-power-explorer](https://github.com/apollo-jhn/windows-power-explorer)** `Python` `CustomTkinter`  
  A desktop inspection tool that allows Windows power users to discover and configure hidden power management schemes and processor performance states.

* **[ParolController](https://github.com/apollo-jhn/ParolController)** `C++` `Arduino Uno` `Firmware`  
  Object-oriented Arduino firmware for an animated Christmas lantern. Features non-blocking software timers, counter-overflow protection, debounced input, and a 5-pattern state machine (awarded 2nd Place Overall).

---

### 💼 Production & Enterprise Platforms

Key production systems I have built and delivered:

* **Flair Platform (Everion Platforms, Inc.)**  
  Creative talent discovery and professional messaging platform. Built backend services with Django 5.2, PostgreSQL, and Celery. Integrated Stripe and Xendit payment rails with automated sub-account verification, Fernet field-level encryption for PII at rest, backfilled automated test suites to ~99.5% coverage across four apps, and built automated CI migration collision gates.

* **EcoSaver ([ecosaver.earth](https://ecosaver.earth)) (Office of the President - Climate Change Commission)**  
  National carbon accounting and sustainability platform. Built core calculation engines and role-gated admin portals with Next.js 16, React 19, and MySQL. Implemented automated PDF certificate generation with Puppeteer and Redis caching layers.

* **People's Survival Fund (Office of the President - Climate Change Commission / Department of Finance)**  
  National climate adaptation financing portal under Republic Act 10174. Engineered multi-track grant application pipelines and role-gated Azure Blob Storage document systems for Philippine local government units.

* **Climate Change Task Force ([cc-taskforce.org](https://cc-taskforce.org)) (Office of the President - Climate Change Commission)**  
  Civic mobilization platform. Created volunteer onboarding workflows with in-browser digital signature capture, photo cropping, and automated digital ID card generation.

---

### 🧰 The Toolkit: Languages & Technologies

I choose the right tool for each project to keep systems fast, maintainable, and reliable.

<p align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="42" alt="Python" title="Python" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg" height="42" alt="Django" title="Django" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="42" alt="TypeScript" title="TypeScript" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" height="42" alt="Next.js" title="Next.js" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="42" alt="React" title="React" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" height="42" alt="PostgreSQL" title="PostgreSQL" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" height="42" alt="Redis" title="Redis" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" height="42" alt="Docker" title="Docker" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg" height="42" alt="Microsoft Azure" title="Microsoft Azure" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/digitalocean/digitalocean-original.svg" height="42" alt="DigitalOcean" title="DigitalOcean" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" height="42" alt="C++" title="C++" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/raspberrypi/raspberrypi-original.svg" height="42" alt="Raspberry Pi" title="Raspberry Pi" />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/arduino/arduino-original.svg" height="42" alt="Arduino" title="Arduino" />
</p>

| Domain | Core Technologies & Production Tools |
| :--- | :--- |
| **💻 Backend & APIs** | Python, Django, Django REST Framework, Django Channels, WebSockets, Celery, Flask |
| **🎨 Frontend & UI** | TypeScript, JavaScript, Next.js (App Router), React 19, Tailwind CSS, Flutter, Zustand |
| **🗄️ Databases & Cache** | PostgreSQL, MySQL, Redis, SQLite |
| **☁️ Cloud & DevOps** | Microsoft Azure, DigitalOcean, Docker, GitHub Actions CI/CD, Linux, Cloudflare |
| **🛡️ Security & Quality** | Fernet PII Encryption, Custom JWT (Device Fingerprint), RBAC, Pytest (~99.5% Coverage), Ruff, CI Migration Gates |
| **🤖 AI Systems & Tooling** | Claude Code, Antigravity, LLM Context Management, Tiktoken, Hugging Face Tokenizers |
| **🔌 Hardware & IoT** | Raspberry Pi (RPi.GPIO), Arduino / ATmega328P, Embedded C++, Sensors & Actuators, LAN/WAN Networking |

---

### 🔥 GitHub Streak & Activity

<div align="center">
  <a href="https://git.io/streak-stats">
    <img src="https://streak-stats.demolab.com?user=apollo-jhn&theme=dark" alt="GitHub Streak" />
  </a>
</div>

---

### 🏆 Honors & Leadership

* **Cum Laude (Latin Honors)**, Bachelor of Science in Computer Engineering, Dr. Filemon C. Aguilar Memorial College of Las Piñas City
* **2nd Place Overall**, Music-Triggered Christmas Lantern (Arduino Parol Firmware) Competition
* **Campus Lead Programmer**, VEX Robotics Competition (November 2024)
* **Open Source Contributor**, GitHub Hacktoberfest (October 2023)

---

### ⚙️ Workflow & Engineering Habits

* **Automation Mindset:** I love writing scripts to automate repetitive daily tasks because building tools that save time is rewarding.
* **Editor Setup:** I write most of my code in **VS Code**, and I use **Vim** for quick edits in the terminal.
* **Coding Soundtrack:** I focus best listening to high-energy synthwave, alternative rock, and metal.
* **Software Meets Hardware:** Debugging embedded hardware circuits with a multimeter is just as fun for me as tracking down complex backend bugs.

---

<div align="center">
  <h3>Ready to build something great? Let's connect! 🚀</h3>
  <p>
    <a href="mailto:japollop.we@gmail.com"><strong>japollop.we@gmail.com</strong></a> | 
    <a href="https://www.linkedin.com/in/john-apollo-ponteras-478036213"><strong>LinkedIn Profile</strong></a> | 
    <a href="https://dev.to/apollo-jhn"><strong>Dev.to Articles</strong></a> | 
    <a href="https://discord.com/users/apollocube"><strong>Discord: apollocube</strong></a>
  </p>
</div>
