# RFC-001: Sample RFC (Caching Layer Example)

## 📌 Metadata
- **RFC ID**: RFC-001
- **Title**: Introduce Caching Layer for API Responses
- **Author(s)**: Jane Doe (SDK), John Smith (Foundry)
- **Created Date**: 2025-09-01
- **Status**: Approved
- **Version**: v1.0
- **Squads**: Foundry, SDK

---

## 1. Motivation
API response times are high due to repeated database queries.  
We need a caching mechanism to reduce latency and improve throughput.

---

## 2. Background / Context
Currently, each request hits the database directly.  
Similar RFCs: RFC-000 (Initial API Architecture).  

---

## 3. Proposal
Introduce a Redis-based caching layer.  

- Cache responses for 5 minutes.  
- Invalidate on database writes.  
- Use client SDK for transparent cache integration.  

See diagram in [`./diagrams/cache-flow.png`](./diagrams/README.md).  
See detailed design in [`design/HLD.md`](./design/HLD.md).  

---

## 4. Alternatives Considered
- In-memory caching → rejected due to limited scalability.  
- CDN caching → rejected due to dynamic responses.  

---

## 5. Impact Analysis
- **Performance**: latency reduced by 60%.  
- **Security**: minimal risk, cache does not store sensitive data.  
- **Compatibility**: no breaking changes.  
- **Operations**: requires Redis cluster.  

---

## 6. Risks & Mitigations
- Cache stampede → mitigated by request coalescing.  
- Stale data → mitigated by short TTL (5 minutes).  

---

## 7. Implementation Plan
1. Deploy Redis cluster.  
2. Update Foundry services to use cache middleware.  
3. Update SDK to fetch from cache if available.  

See [`design/HLD.md`](./design/HLD.md) and [`design/LLD.md`](./design/LLD.md) for details.  

---

## 8. Rollout & Monitoring
- Rollout behind feature flag.  
- Monitor cache hit rate, latency, DB load.  
- Rollback → disable feature flag.  

---

## 9. Changelog
- v1.0 – Approved initial design.  

---

## 10. References
- Redis Docs: https://redis.io  
- Prior RFCs: RFC-000 (API Architecture)  
- Notes: [`notes/meeting-notes.md`](./notes/meeting-notes.md)  
