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
    String[] learning = { "Distributed Systems", "Concurrency", "PostgreSQL Internals", "DSA" };
    String openTo     = "Backend / SDE Internships";
}
```

---

### Tech Stack

**Languages**
<br/>
![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white)

**Backend & Frameworks**
<br/>
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.4-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

**Databases & Caching**
<br/>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_16-316192?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis_7.2-DC382D?style=flat-square&logo=redis&logoColor=white)

**Testing, Observability & DevOps**
<br/>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

---

### Featured Projects

#### 1. [Sentinel API Gateway](https://github.com/lithincg/sentinel-api-gateway) · [Live Demo](https://sentinel-api-gateway-pimj.onrender.com)
`Java 21` `Spring Boot 3.4` `Spring Security` `Redis 7.2` `PostgreSQL 16` `Lua` `Docker` `Prometheus` `Grafana` `k6`
- Cut API latency under 50 concurrent users by **96.6%** (`439ms → 15ms` avg, `761ms → 27ms` P95) and scaled throughput **24x** (`112 → 2,744 req/s`) by caching SHA-256 API key lookups in Redis ahead of BCrypt.
- Built dual stateless authentication (JWT user sessions + hashed API keys) with isolated security filter chains.
- Engineered distributed rate limiting with Redis Sorted Sets and atomic Lua scripts (`HTTP 429` + `Retry-After`) with local memory and DB fallback during Redis outages.
- Verified with 15 JUnit 5 concurrency tests (`1,000` concurrent threads), Testcontainers PostgreSQL checks, and 4 k6 load scenarios.

#### 2. [Sova (Distributed Job Scheduler)](https://github.com/lithincg/sova)
`Java 21` `Spring Boot 3.4` `PostgreSQL 16` `Redis 7.2` `Flyway` `Docker Compose` `Testcontainers` `Prometheus` `GitHub Actions`
- Built a concurrent job claiming engine using PostgreSQL `FOR UPDATE SKIP LOCKED` and partial indexes, verified across 8 concurrent threads claiming 40 jobs with **0 duplicate claims and 0 lost jobs**.
- Implemented automatic worker crash recovery via expiring 30s Redis heartbeats and a background reaper, paired with capped exponential backoff retries, dead letter queues, and manual replay APIs.
- Added idempotent job submission (`Idempotency-Key` partial unique index), guarded state transitions, and attempt execution history endpoints.
- Instrumented Micrometer/Prometheus counters (`completed`, `retried`, `reclaimed`) with automated Testcontainers integration tests in GitHub Actions CI.
