<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=180&section=header&text=Anubhav%20Bisht&fontSize=48&fontColor=ffffff&fontAlignY=35&desc=I%20build%20LLM%20agents%20that%20do%20real%20work&descSize=16&descAlignY=55" width="100%" />

<a href="https://github.com/anubhavbisht"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&width=620&lines=LangGraph+state+machines+in+TypeScript;Agents+that+stop+for+a+reason%2C+not+a+token+budget;RAG+pipelines+%C2%B7+tool+calling+%C2%B7+multi-agent+routing;Distributed+backends+with+NestJS+%2B+Nx" alt="what I build" /></a>

<br/>

<a href="https://www.linkedin.com/in/anubhavbisht/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:anubhavbisht98@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://leetcode.com/anubhavbisht98/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" /></a>

</div>

---

### About me

Full-stack developer working my way down the stack into **AI agent engineering**.

Most of what I ship now is built on **LangGraph in TypeScript**: agents with explicit
state machines, tool calls that hit real APIs, and loops that stop for a reason rather
than when a token budget runs out. I care about the parts people skip — routing you can
test, revision caps, grounded stopping conditions, tracing.

- Currently building — multi-agent systems: Reflexion loops, RAG pipelines, tool-using assistants
- Currently learning — evaluation & observability for LLM apps (Langfuse, OpenTelemetry), NestJS, DSA
- Ask me about — LangGraph state machines, RAG, tool calling, TypeScript, Bun, Node
- Also on — [LeetCode](https://leetcode.com/anubhavbisht98/) · [InterviewBit](https://www.interviewbit.com/profile/anubhav-bisht)
- Reach me — [LinkedIn](https://www.linkedin.com/in/anubhavbisht/) · anubhavbisht98@gmail.com

---

### What I'm building

**AI agents** — LangGraph state machines in TypeScript, each one a different pattern.

| Project | Pattern it demonstrates |
|---|---|
| **[research-agent](https://github.com/anubhavbisht/research-agent)** | **Reflexion.** One model drafts an answer, critiques its own draft, searches for what it admitted was missing, and rewrites — until every claim rests on a source or the revision budget runs out. `LangGraph · OpenAI · Tavily · Bun` |
| **[customer-support-chatbot-agent](https://github.com/anubhavbisht/customer-support-chatbot-agent)** | **Multi-agent routing.** A front desk triages each question and hands it to the specialist that owns it; the learning specialist answers from course docs via RAG, not model memory. `LangGraph · Groq · Pinecone · Nomic` |
| **[calendar-agent](https://github.com/anubhavbisht/calendar-agent)** | **Tool calling against a live API.** "Move Friday's meeting to 3pm and invite priya@" — and it does, on the real Google Calendar. `LangGraph · Google Calendar API` |
| **[linkedin-writer-post](https://github.com/anubhavbisht/linkedin-writer-post)** | **Writer/critic loop.** A writer drafts, a critic scores against a shared rubric, and the draft goes back until it passes or the budget runs out. `LangGraph · Groq` |
| **[doc-based-internal-chat-using-rag](https://github.com/anubhavbisht/doc-based-internal-chat-using-rag)** | **RAG with a fallback.** Ingests a PDF, embeds it, answers grounded in that document — and falls through to live web search for real-time questions. `RAG · Express · Tailwind` |
| **[graph-vs-agent](https://github.com/anubhavbisht/graph-vs-agent)** | **Why the abstraction exists.** The same chatbot three ways: a prebuilt `createAgent()`, a hand-written `StateGraph`, and a graph with no LLM at all — to isolate graph mechanics from the AI. |

**Backend & distributed systems**

#### [ds-job](https://github.com/anubhavbisht/ds-job) — a distributed job engine

Not an agent, and deliberately so. A job engine has to survive the things a chat loop
never faces: work that outlives the request that created it, executors that die
mid-run, and a scheduler that must not hand the same job to two workers.

Built as an **Nx monorepo of four NestJS services**, split along the failure boundaries:

| Service | Owns |
|---|---|
| `auth` | Identity and tokens — the only service that talks to the user directly |
| `jobs` | The job registry and scheduling. Decides *what* runs and *when* |
| `executor` | Runs the work. Isolated so a crashing job takes down one worker, not the scheduler |
| `products` | The domain service the jobs act on |

Talking over `@nestjs/microservices`, persisted with **Prisma on PostgreSQL**, each
service owning its own schema so none of them reaches into another's tables.

`TypeScript · NestJS · Nx · Prisma · PostgreSQL`

<br/>

| Also | |
|---|---|
| **[expense-agent](https://github.com/anubhavbisht/expense-agent)** | Terminal finance assistant. Tool calling written from scratch, including retries around Groq's intermittent `tool_use_failed`. `Bun · Groq` |

<sub>Also poking at: [tdd](https://github.com/anubhavbisht/tdd) · [os_concurrency](https://github.com/anubhavbisht/os_concurrency) · [learning-low-level-design](https://github.com/anubhavbisht/learning-low-level-design) · [invoking-llm](https://github.com/anubhavbisht/invoking-llm)</sub>

---

### Tech

**Languages**
<p>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white" />
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" />
</p>

**AI / Agents**
<p>
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/Groq-F55036?style=flat-square&logo=lightning&logoColor=white" />
<img src="https://img.shields.io/badge/Pinecone-000000?style=flat-square&logo=pinecone&logoColor=white" />
<img src="https://img.shields.io/badge/Langfuse-000000?style=flat-square&logo=opentelemetry&logoColor=white" />
<img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white" />
</p>

**Runtime & Web**
<p>
<img src="https://img.shields.io/badge/Bun-000000?style=flat-square&logo=bun&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" />
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
</p>

**Data & Tools**
<p>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white" />
<img src="https://img.shields.io/badge/Nx-143055?style=flat-square&logo=nx&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
</p>

---

### GitHub

<div align="center">

<img height="165" src="https://github-readme-stats-eight-tau-20.vercel.app/api?username=anubhavbisht&show_icons=true&hide=stars,issues&hide_rank=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=58A6FF&text_color=C9D1D9" />
<img height="165" src="https://github-readme-stats-eight-tau-20.vercel.app/api/top-langs/?username=anubhavbisht&layout=compact&langs_count=6&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9" />

<img height="165" src="https://streak-stats.demolab.com?user=anubhavbisht&theme=tokyonight&hide_border=true&background=0D1117&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF" />

<br/><br/>

<!-- Generated in this repo by .github/workflows/snake.yml - appears after the workflow's first run -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/anubhavbisht/anubhavbisht/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/anubhavbisht/anubhavbisht/output/github-snake.svg" />
  <img alt="contribution snake" src="https://raw.githubusercontent.com/anubhavbisht/anubhavbisht/output/github-snake.svg" width="98%" />
</picture>

</div>

---

<div align="center">
<sub>Building in public. Every repo above has a README that explains <em>why</em> it's built that way, not just how to run it.</sub>
</div>
