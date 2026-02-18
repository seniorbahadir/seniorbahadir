<!--
PROFILE README
Theme: Calm Systems, Sharp Edges
Goal: In 15 seconds, visitors understand what you build and how you think.
-->

<h1 align="center">Hi, I'm Bahadır 👋</h1>

<p align="center">
  Backend Engineer focused on <b>boring-in-production</b> systems: secure, observable, and scalable.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/bahadir-kayhan-31a55a1b2">LinkedIn</a> •
  <a href="mailto:kayhan1901@gmail.com">Email</a>
</p>

<p align="center">
  <b>.NET</b> • <b>Microservices</b> • <b>API Gateway</b> • <b>Auth</b> • <b>Event-Driven</b> •
  <b>Kafka/Debezium</b> • <b>RabbitMQ</b> • <b>Redis</b> • <b>SQL Server + MongoDB</b> • <b>Production Reliability</b>
</p>

<p align="center">
  <img alt=".NET" src="https://img.shields.io/badge/.NET-512BD4?logo=dotnet&logoColor=white" />
  <img alt="SQL Server" src="https://img.shields.io/badge/SQL%20Server-CC2927?logo=microsoftsqlserver&logoColor=white" />
  <img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white" />
  <img alt="Kafka" src="https://img.shields.io/badge/Kafka-231F20?logo=apachekafka&logoColor=white" />
  <img alt="RabbitMQ" src="https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white" />
  <img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" />
</p>

---

## 🎯 Now
- Building **audit/event pipelines** (CDC → Kafka → MongoDB) with idempotent ingestion
- Designing **gateway-first** microservice access (auth, routing, rate limiting, health checks)
- Keeping systems **predictable**: clean contracts, clear boundaries, safe failure modes

---

## ⚙️ What I work on
- **.NET backend engineering** with clean layering (API / Application / Domain / Infrastructure)
- **Microservices** with strong contracts, predictable behavior, and clear boundaries
- **API Gateway patterns** (routing, centralized auth, rate limiting, health checks)
- **Authentication & security** (JWT, refresh-token rotation, OTP-first flows)
- **Event-driven systems** (Kafka, Debezium CDC, RabbitMQ messaging, Redis caching)
- **Data foundations** (SQL Server, stored procedures, pragmatic ADO.NET mapping, MongoDB event stores)

---

## 🧠 Engineering principles
- **Make failures boring:** idempotency, retries, timeouts, and clear error contracts  
- **Design for observability:** traceable flows, structured logs, actionable signals  
- **Keep contracts stable:** consistent naming, small PRs, reviewable change sets  

---

## 🧩 Featured projects (pin these)
> Replace links with your real repos when ready.

- **Audit Pipeline (CDC → Kafka → MongoDB)**  
  Why: production-grade audit trail  
  Highlights: Debezium connector, Kafka consumer worker, idempotent ingestion, timeline viewer  
  Repo: `https://github.com/seniorbahadir/<audit-pipeline-repo>`

- **API Gateway (.NET)**  
  Why: a single secure entry point  
  Highlights: centralized JWT verification, token forwarding, rate limiting, health checks  
  Repo: `https://github.com/seniorbahadir/<api-gateway-repo>`

- **Shared Data Provider (MongoDB)**  
  Why: reusable foundation across services  
  Highlights: cached client/db approach, named connections, DI-first design, optional health checks  
  Repo: `https://github.com/seniorbahadir/<mongo-provider-repo>`

---

## 🗺️ Architecture snapshot
<details>
  <summary><b>Show diagram</b></summary>

```mermaid
flowchart LR
  A[Clients] --> G[API Gateway]

  G --> S1["Service A (.NET)"]
  G --> S2["Service B (.NET)"]

  S1 --> M[(SQL Server)]
  M --> D[Debezium]
  D --> K[(Kafka)]
  K --> C["Audit Consumer (.NET Worker)"]
  C --> O[(MongoDB)]
  O --> V["Audit Viewer UI"]

  S1 --> R[(Redis Cache)]
  S2 --> Q[(RabbitMQ)]
