---
layout: page
title: Agentic AI HotelBot
description: AI-powered virtual concierge for luxury hotels using GPT, LangGraph agents, LlamaIndex, FastAPI, Redis, and Neon PostgreSQL. Supports room booking, FAQ search, and real-time availability. Deployed via Docker on Hugging Face and AWS ECS.
img: assets/img/z13a.jpg
importance: 3
category: [Generative AI]
related_publications: false
---

<!-- ### **Case Study: AI-Driven Rare Disease Research Collaborative Network** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z13a.png" title="    Agentic AI-Powered Virtual Concierge for Luxury Hotels" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Agentic AI-Powered Virtual Concierge for Luxury Hotels.
</div>

---

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/img1.png" title="AI-Driven Rare Disease Research Collaborative Network" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
   End-to-End Architecture of the AI-Driven Rare Disease Research Collaborative Network (RCN): This diagram illustrates the data flow from biomedical data sources (PubMed, NIH Grants, Clinical Trials) through graph-based modeling, clustering, expertise summarization with fine-tuned LLMs, and Retrieval-Augmented Generation (RAG) to deliver personalized specialist recommendations using agent-based query parsing.
</div>


# Blue Horizon AI Concierge
**AI-Powered Virtual Concierge for Luxury Hotels**

---

## AI-Powered Guest Interaction & Real-Time Booking

**The Blue Horizon AI Concierge** is a full-stack virtual assistant system that brings natural language interaction to luxury hospitality. It interprets guest queries using LLMs, enables real-time room bookings, and provides intelligent, context-aware responses for FAQs and hotel services.

---

## 1. Introduction
Luxury hotels often lack scalable, conversational systems to manage dynamic guest inquiries, real-time booking, and service personalization. Blue Horizon solves this by integrating state-of-the-art LLMs, semantic search, and multi-agent coordination to build a real-time concierge application with seamless frontend-backend communication.

---

## 2. Key Questions Addressed
- How can we use natural language understanding for hotel bookings?
- Can LLMs interpret unstructured guest queries and convert them into database actions?
- How can a dynamic FAQ system improve guest experience?
- How do we deploy a scalable concierge application with minimal latency?

---

## 3. The Problem
- Traditional booking systems are rigid and rule-based.
- Guests need to rephrase queries to match the system.
- FAQs are static and non-personalized.
- Hotel systems don’t utilize real-time data pipelines or multi-agent intelligence.

---

## 4. The Importance
- Increases guest satisfaction through intelligent, real-time responses.
- Automates concierge services, reducing staff workload.
- Enables dynamic pricing and booking via real-time database queries.
- Provides flexible deployments through Docker, Hugging Face, and AWS.

---

## 5. The Solution

### 5.1 Conversational Intelligence
- Uses OpenAI GPT for query parsing.
- Implements NL-to-SQL conversion for booking intent via a dedicated agent.

### 5.2 Multi-Agent Orchestration with LangGraph
- **Modeled agentic AI using LangGraph**, where a **supervising agent** manages reasoning and memory across the interaction lifecycle.
- The supervising agent coordinates:
  - A **RAG agent** (Retrieval-Augmented Generation) to handle FAQ and policy lookups.
  - A **SQL agent** that converts natural language into SQL to check real-time room availability.

### 5.3 Semantic Search
- Leverages LlamaIndex and Sentence Transformers to retrieve FAQ responses based on vector similarity.

### 5.4 Real-Time Data Pipelines
- Connects to Neon PostgreSQL for structured data (room types, pricing, availability).
- Uses Redis for caching and vector lookups.

### 5.5 Modular Backend
- Built on FastAPI for scalable API serving.
- Agent-based orchestration ensures modularity and fault tolerance.

### 5.6 Guest-Facing Interface
- Deployed Streamlit frontend integrates real-time chat and booking pipeline.

---

## 6. Architecture Overview
**End-to-End Flow:**  
Natural language query → Supervisor Agent (LangGraph) → RAG Agent + SQL Agent → Response Generation → Streamlit UI

---

## 7. Results & Impact
- Interprets diverse guest queries (e.g., “Can I get a king room with a sea view for tomorrow night?”).
- Vector-based FAQ search yields semantically relevant answers with top-k ranking.
- Real-time availability checks via SQL queries to Neon PostgreSQL.
- Seamless user interaction through a modern, responsive Streamlit interface.
- Deployable via Docker to Hugging Face Spaces and AWS ECS (Fargate).

---

## 8. Skills and Tools Used

| Category            | Technologies                                                                 |
|---------------------|------------------------------------------------------------------------------|
| AI/NLP              | OpenAI GPT-4, Sentence Transformers, LlamaIndex                              |
| Multi-Agent System  | LangGraph, Langchain Agents                                                  |
| Backend             | FastAPI, Redis                                                               |
| Frontend            | Streamlit                                                                    |
| Databases           | Neon PostgreSQL, Redis                                                       |
| Deployment          | Docker, Hugging Face Spaces, AWS ECR & ECS                                   |
| Dev Tools           | Poetry, Uvicorn, Pytest, Pydantic                                            |

---

## 9. Future Directions
- Integrate multimodal search (e.g., images or reviews).
- Add multilingual support for international guests.
- Improve CoT prompting for ambiguous guest queries.
- Enable smart notifications and reservation tracking.
- Connect to IoT for room service and facility access.

---

## 10. Generative AI Capabilities
- **Semantic Query Understanding:** Natural language interpretation and slot-filling.
- **Agentic Reasoning:** LangGraph-powered agent with memory and decision control.
- **Vector-Based Retrieval:** Embedding-driven response generation using LlamaIndex.
- **NL2SQL Reasoning:** Translates guest questions to SQL queries for real-time bookings.
- **Multi-Agent Collaboration:** Supervisor agent coordinates RAG and SQL agents.
- **Flexible Deployment:** Supports deployment to Docker, Hugging Face, and AWS ECS with scalable architecture.

---

**© 2025 Jaber Valinejad. Powered by Docker, LangGraph, and Streamlit. Hosted on Hugging Face and AWS.**

