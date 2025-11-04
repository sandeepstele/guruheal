# Guruheal — AI-Powered Healthcare Assistant

<p align="center">
  <strong>Intelligent healthcare assistant</strong> — Ayurvedic & holistic wellness, powered by AI
</p>

<p align="center">
  <a href="https://v0-guruheal-presentation.vercel.app"><strong>Explore live demo →</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open_Source-MIT-green?style=for-the-badge" alt="Open Source" />
  <img src="https://img.shields.io/badge/Stack-Microservices-6C63FF?style=for-the-badge" alt="Microservices" />
</p>

### Built with

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind" />
  <img src="https://img.shields.io/badge/Radix_UI-161618?style=flat-square&logo=radixui&logoColor=white" alt="Radix UI" />
  <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=black" alt="Supabase" />
  <br />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/LightRAG-RAG_Engine-FF6B35?style=flat-square&logo=huggingface&logoColor=white" alt="LightRAG" />
</p>

---

Welcome to **Guruheal**. Guruheal is an intelligent healthcare assistant application designed to streamline healthcare services with advanced AI capabilities, focused on Ayurvedic and holistic wellness.

**Explore the live application and detailed presentation:** [Guruheal Application Presentation](https://v0-guruheal-presentation.vercel.app)

---

## Open-Source Note

This project was developed inside an organization and has been open-sourced. The codebase is now publicly available for use and contribution.

---

## Overview

Guruheal integrates multiple microservices to deliver a seamless and intelligent healthcare experience. Below are the core components of the system.

### Microservices

1. **Agent Service (Backend — FastAPI)**

   The backend agent microservice powers the GuruHeal AI chat for Ayurvedic and holistic wellness. It provides a streaming chat API, conversation history stored in PostgreSQL (Supabase), RAG-backed knowledge-base search via an external RAG service, and optional live web search with sources cached in Redis. Responses support Hindi, Tamil, Telugu, Kannada, and English. The agent returns metadata with citations, suggested follow-up questions, and auto-generated conversation titles.

   **Tech:** FastAPI, Pydantic AI, OpenAI-compatible LLM, PostgreSQL (Supabase), Redis, Logfire.

   Repository: [guruheal-agent](https://github.com/sandeepstele/guruheal-agent)

2. **Chat Service (Frontend — Next.js)**

   The user-facing frontend provides the conversational interface for interacting with Guruheal’s AI assistant. It includes a streaming chat UI, conversation sidebar to list, create, and switch conversations, a sources panel for citations and links, follow-up questions, optional Supabase auth, text-to-speech for replies, PDF export of responses, and light/dark theme support.

   **Tech:** Next.js 15, React 19, TypeScript, Tailwind CSS, Radix UI, Supabase.

   Repository: [guruheal-chat](https://github.com/sandeepstele/guruheal-chat)

3. **RAG Service (Backend — LightRAG)**

   A retrieval-augmented generation (RAG) and knowledge-graph service built on [LightRAG](https://github.com/HKUDS/LightRAG). It indexes documents (e.g. Ayurveda, wellness), maintains a knowledge graph, and exposes a query API (`POST /query`, `POST /query/stream`) used by the GuruHeal Agent for knowledge-base search. An optional Web UI supports document indexing and exploration.

   **Tech:** Python, LightRAG, FastAPI. Configurable LLM/embeddings (OpenAI, Ollama, Hugging Face, etc.).

   Repository: [rag-service](https://github.com/sandeepstele/rag-service)

---

## Additional Services

- **Web Search Agent** — Reused from the deployed service in the Vessel Match project to provide web search capabilities for enhancing AI responses.

---

## How to Use

Each microservice can be cloned and deployed independently. Follow the setup instructions in their respective repositories to get started.

To experience the full application, visit the [live Guruheal presentation](https://v0-guruheal-presentation.vercel.app) for demos and detailed walkthroughs.

---

## Contributors

- [sandeepstele](https://github.com/sandeepstele)
- [trishulam](https://github.com/trishulam)

---

## Contact & Contributions

For questions, suggestions, or collaboration opportunities, feel free to open an issue in any of the above repositories or contact the maintainers.

Thank you for your interest in Guruheal.
