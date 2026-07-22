<h1 align="center">Hi, I'm Eneko 👋</h1>

<p align="center">
  <b>Software Engineer</b> · Applied AI · Agent Tooling · Production Systems
</p>

<p align="center">
  <a href="https://github.com/Enraxk">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=900&center=true&vCenter=true&width=650&lines=Applied+AI%3A+RAG+pipelines+and+agent+tooling;MCP+servers+in+production%2C+used+daily;React+%2B+TypeScript+%2B+.NET+at+enterprise+scale;Production+systems%2C+end+to+end" alt="Typing SVG" />
  </a>
</p>

---

## About me

- 📍 Based in **Madrid, Spain**
- 🛠️ I build **production systems end to end**: AI infrastructure, backends, and enterprise frontends
- 🧠 Right now: **retrieval pipelines**, **Model Context Protocol servers**, and the platform layer that runs them
- 🔍 I care about getting things **measured**, not assumed. See below.
- 🔒 Client work ships to private repos. What I can open, I open, starting with **naeth**.

---

## What I'm building

**[naeth](https://github.com/Enraxk/naeth)** · portable memory for AI agents
Postgres + pgvector (HNSW), hybrid retrieval fusing semantic and lexical search with RRF, event-sourced append-only store, async embedding worker. Exposed to LLM clients as 8 MCP tools behind OAuth 2.1. Running in production and used daily from Claude Code and claude.ai.

**[cenit](https://github.com/Enraxk/cenit)** · modular self-hosted platform
A Terraform-style reconciler (`plan` / `apply`, idempotent) that wires each module's identity, ingress, secrets and lifecycle from a single YAML manifest. Runs the identity and exposure layer in front of my own services.

**GridWatch** · enterprise IoT platform (client work, private)
React 19 + TypeScript frontend of a platform monitoring 10,000+ devices in real time for electricity distribution networks. ~33,500 LOC, 80+ views, primary contributor.

**Yogin** · SaaS billing backend (freelance, private)
Node + Express + MongoDB. Per-class payments aggregated into monthly invoices, immutable price snapshots, scheduled invoicing and adjustments, from schema ADR to production. I own the client relationship directly: scoping, written proposals, pricing and delivery.

---

## Measured, not guessed

- **Retrieval.** Benchmarked embedding models against my own corpus and migrated to `multilingual-e5-large`: recall@1 of 0.80 vs 0.56 for the previous model.
- **Tool descriptions.** Isolated description language as a variable in agent tool retrieval and ran a controlled test: 5/5 hits in English vs 0/5 in Spanish. Rewrote every tool description on that evidence.
- **Security.** Put an automated audit of a production platform through an adversarial verification pass: 88 raw findings down to the 27 that survived scrutiny, each one reproduced before it was reported.

---

## Open problems

What I am working through right now, and the constraint that makes each one interesting.

- **Identity that survives across machines.** `cenit` runs on a single node today. A second node means one login that holds across both without inventing a single point of failure. The design is verified, the build is next. The constraint that shapes it: putting a conventional auth proxy in front of an MCP endpoint breaks remote MCP clients, so "protect every route" cannot be solved the obvious way.
- **Direct manipulation over a knowledge graph.** The `naeth` viewer is being rewritten in Svelte 5 so that relating two notes is a drag, not a form. Easy to demo, hard to make good with touch input. Panels first, floating window manager last and only if it still itches, because that is where projects like this usually die.
- **What an agent should be trusted to declare.** MCP carries no signal of which model is on the other end, so authorship has to separate what the client proves from what the agent claims. I shipped that split, then enabled strict enforcement only after measuring that real clients declare it unprompted.

**Retired:** `comfy-mcp`, an image generation MCP server. I built it, used it, and concluded the need was not real. Tunnel, DNS and connectors removed, code archived, and the two lessons that generalized written down. Knowing what to delete is part of the job.

---

## Tech stack

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,fastapi,postgres,docker,linux,git&perline=6" />
</p>
<p align="left">
  <img src="https://skillicons.dev/icons?i=react,ts,nextjs,svelte,dotnet,nodejs,azure&perline=7" />
</p>

---

## Writing samples

- 🧩 Code sample (sanitized excerpt): https://gist.github.com/Enraxk/b29514a2a8029affc262ffdcf7576b4a
- ✍️ Technical writing sample: https://gist.github.com/Enraxk/d38340e1ab653f9569763e05c321c6b5

---

## Contact

- 💼 LinkedIn: https://www.linkedin.com/in/eneko-lapuente-bascu%C3%B1ana/
- 📫 Email: enekolapuentebas@gmail.com
- 🌍 Open to **remote** and **Madrid-based** opportunities
