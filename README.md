# Hi, I'm Le Nhat Duy 👋
### Backend & Systems Engineer | Specializing in Scalable Architectures & Data Pipelines

I am a Software Engineering student at the **University of Science (VNU-HCM)**, majoring in **Computer Networks and Telecommunications** (GPA: **8.18 / 10**). I design and deploy reliable, high-concurrency backend systems, real-time IoT event pipelines, and memory-efficient storage architectures. 

My engineering philosophy is simple: **build production-grade software that is reliable, secure, and optimized for real-world hardware limits.**

---

## 🚀 Featured Project: TDMedia Studio
> **Live Production Platform:** [tdmedia.site](https://tdmedia.site) | **Role:** Core Backend Architect & DevOps

A production photo album management platform serving real-world photography clients. Engineered to handle large concurrent file uploads and asynchronous processing pipelines on resource-constrained host servers (deployed via Docker on Synology NAS).

### 🛠️ Key Architectural & Performance Wins:
- **Zero-Buffer Streaming Uploads**: Utilized Node.js `Busboy` to stream multi-file multipart uploads directly to disk without memory buffering, preventing server out-of-memory crashes under heavy concurrent usage.
- **Nginx X-Accel-Redirect Integration**: Bypassed Node.js event-loop overhead for media serving by using Nginx `internal` locations. The NestJS API verifies download JWTs and offloads direct file streaming to Nginx, reducing Node.js CPU usage by **over 60%**.
- **Asynchronous Task Queues**: Built a robust background processing pipeline using Redis and BullMQ. Offloaded WebP image compression (Sharp), thumbnail generation, and ZIP archive bundling to concurrent background workers.
- **Transaction-Safe Operations**: Designed custom job tracking handlers in BullMQ to handle client-side abort signals. On job cancellation (`JobCancelledError`), workers automatically clean up temporary disk resources and synchronize PostgreSQL database transaction states.

---

## 📁 Key Engineering Repositories

### 📡 Flood Sense Tunnel
*Real-time IoT Telemetry & Environmental Monitoring System*
- **Ingestion Pipeline**: Designed a high-throughput telemetry ingestion pipeline using an MQTT broker to capture live sensor streams from remote nodes.
- **Real-time Broadcast**: Built customized, low-latency WebSocket connection pools to broadcast live telemetry metrics to active client dashboards.
- **Optimized Storage**: Modeled an optimized MongoDB database structure for time-series sensor logs, reducing query response latencies and storage footprint.
- **DevOps**: Containerized the application with Docker and configured automated health checks on a VPS deployment.

### 📦 Enterprise Inventory & Invoice System (Java / Spring Boot)
*Sales, Warehouse & Invoice Management SaaS for Vietnamese Merchants*
- **Java Spring Boot Backend**: Built a structured multi-layered API (Spring Boot 3, Spring Security, Spring Data JPA) optimized for local businesses.
- **AWS S3 / Cloudflare R2 Uploads**: Implemented a memory-efficient upload pipeline using S3 SDK Presigned URLs, enabling clients to upload raw invoice files directly to Cloudflare R2 and avoiding server-side bandwidth exhaustion.
- **Secure CDN Delivery**: Secured private files using short-lived (15-min) Presigned GET URLs issued dynamically by Spring Boot after checking user permissions.
- **Zero Inbound Port Routing**: Containerized in Docker and routed traffic securely using a Cloudflare Tunnel (`iostream.store`), eliminating firewall vulnerabilities and host IP exposure.

---

## 🛠️ Technology Stack & Expertise

| Category | Technologies |
| :--- | :--- |
| **Backend Core** | TypeScript, JavaScript, Node.js, NestJS, Spring Boot (Java), Express.js |
| **Databases & Caching** | PostgreSQL, MongoDB, Redis, Prisma ORM, Spring Data JPA |
| **Real-time & Queues** | MQTT, WebSocket, BullMQ (Task Queue Processing) |
| **Infrastructure & DevOps** | Docker, Nginx, Cloudflare Tunnels, Cloudflare R2, Linux VPS, Jenkins, Git/GitHub Actions |
| **Testing & Tools** | Jest, Supertest, Postman, Swagger/OpenAPI |

---

## 🧠 Architectural Interests & Focus
- **Distributed Queues & Worker Patterns**: High-throughput jobs, rate-limiting, and error-recovery.
- **Memory-Efficient Data Processing**: I/O stream piping, buffer minimization, and server-side CPU offloading.
- **Defensive Security Practices**: Preventative designs against Directory Traversal, secure session/token management, and zero-trust network configurations.

---

## 📬 Connect With Me
- **Email:** [lnhatduy27@gmail.com](mailto:lnhatduy27@gmail.com)
- **LinkedIn:** [linkedin.com/in/lnhatduy27](https://www.linkedin.com/in/lnhatduy27)
- **Flagship Project:** [tdmedia.site](https://tdmedia.site)
