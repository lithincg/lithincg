<div align="center">

# Hi, I'm Lithin C G

**B.Tech CS Undergrad @ VIT-AP University · Java Backend & Distributed Systems**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/lithin-c-g)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lithinraju1@gmail.com)
[![Sentinel Live](https://img.shields.io/badge/Sentinel_Live_Demo-166534?style=for-the-badge&logo=render&logoColor=white)](https://sentinel-api-gateway-pimj.onrender.com)

</div>

---

### About Me

```java
public class Lithin {
    String location   = "Bengaluru, India";
    String education  = "B.Tech CSBS @ VIT-AP University (2028)";
    String focus      = "Java Backend Engineering & Distributed Systems";
    String[] building = { "Sentinel API Gateway", "Sova Job Scheduler" };
    String[] learning = { "Distributed Systems", "Concurrency", "Microsoft Azure", "DSA" };
    String openTo     = "Backend / SDE Internships";
}
```

---

### Tech Stack

**Languages**
<br/>
![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white)

**Backend & Frameworks**
<br/>
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.4-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Spring MVC](https://img.shields.io/badge/Spring_MVC-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Micrometer](https://img.shields.io/badge/Micrometer-1C1917?style=flat-square)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

**Databases & Caching**
<br/>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_16-316192?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis_7.2-DC382D?style=flat-square&logo=redis&logoColor=white)

**Testing, Observability & DevOps**
<br/>
![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white)
![Mockito](https://img.shields.io/badge/Mockito-78A641?style=flat-square)
![Testcontainers](https://img.shields.io/badge/Testcontainers-2596BE?style=flat-square)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black)
![Neon](https://img.shields.io/badge/Neon-00E599?style=flat-square)
![Upstash](https://img.shields.io/badge/Upstash-00E9A3?style=flat-square&logo=upstash&logoColor=black)

---

### Featured Projects

#### 1. [Sentinel API Gateway](https://github.com/lithincg/sentinel-api-gateway) · [Live Demo](https://sentinel-api-gateway-pimj.onrender.com)
`Java 21` `Spring Boot 3.4` `Spring Security` `Redis 7.2` `PostgreSQL 16` `Lua` `Flyway` `Docker` `JUnit 5` `Testcontainers` `Prometheus` `Grafana` `k6`
- Cut API latency under 50 concurrent users by **96.6%** (`439ms → 15ms` avg, `761ms → 27ms` P95), scaled throughput **24x** (`112 → 2,744 req/s`), and reduced authentication contention errors from **16.1% to 1.8%** by caching SHA-256 API key lookups in Redis ahead of BCrypt.
- Built dual stateless authentication (JWT user sessions + hashed API keys) with isolated security filter chains, PostgreSQL API key management endpoints (issue, list, revoke) via Flyway, 404 ownership checks on unauthorized access, and instant Redis cache eviction on revocation.
- Engineered distributed rate limiting using Redis Sorted Sets and atomic Lua scripts (`HTTP 429` + `Retry-After`) paired with concurrent local memory and database fallback during Redis outages.
- Automated 15 JUnit 5 concurrency tests (`1,000` concurrent threads) and Testcontainers PostgreSQL checks; deployed on Render, Neon, and Upstash with Prometheus, Grafana, and 4 k6 load scenarios.

#### 2. [Sova (Distributed Job Scheduler)](https://github.com/lithincg/sova)
`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Redis 7.2` `Flyway` `Docker` `Docker Compose` `GitHub Actions` `JUnit 5` `Testcontainers` `Prometheus`
- Built a concurrent job claiming engine using PostgreSQL `FOR UPDATE SKIP LOCKED` and partial indexes, verified across 8 concurrent threads claiming 40 jobs with **0 duplicate claims and 0 lost jobs**.
- Implemented automatic worker crash recovery via expiring 30s Redis heartbeats and a background reaper, paired with capped exponential backoff retries, dead letter queues, and manual replay APIs.
- Added idempotent job submission (`Idempotency-Key` partial unique index), guarded state transition rules, and attempt history REST endpoints recording worker ID, duration, and errors.
- Instrumented Prometheus counters (`completed`, `retried`, `reclaimed`) alongside structured logging, graceful shutdown, local two worker Docker Compose orchestration, and automated Testcontainers integration tests in GitHub Actions CI.
