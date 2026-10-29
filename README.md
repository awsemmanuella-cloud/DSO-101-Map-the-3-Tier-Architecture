# DSO-101-Map-the-3-Tier-Architecture
PostureSec follows a 3-tier architecture with clear separation between the presentation layer, application layer, and data layer. Each tier has defined ports and trust boundaries.

---

## Tier Breakdown

### 1. Frontend Tier
- **Technology:** React served by Nginx
- **Ports:** 80 (HTTP) and 443 (HTTPS)
- **Trust Boundary:** Public-facing (accessible from the internet)

### 2. Backend Tier
- **Technology:** Node.js + Express
- **Port:** 3000
- **Trust Boundary:** Private / Internal (only accessible by the frontend or internal services)

### 3. Database Tier
- **Technology:** PostgreSQL
- **Port:** 5432
- **Trust Boundary:** Internal-only (never exposed to the public internet)

---

## Why the Database is Never Public-Facing

The database is deliberately kept internal for security reasons:

- It should only be reachable by the backend application.
- Exposing the database directly to the internet would create a major security risk (attackers could try to connect to it).
- By keeping it internal-only, we reduce the attack surface and protect sensitive data.

This is a core principle of secure architecture: **only expose what must be public**.

---

**This mapping shows the tiers, ports, and trust boundaries required by DSO-101.**
---

## Architecture Diagram attached

## Documented by:* Emmanuella Blessing Udeh  
*Date:* October 2026

