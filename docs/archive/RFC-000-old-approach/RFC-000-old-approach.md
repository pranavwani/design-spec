# RFC-000: Legacy Auth System

## 📌 Metadata
- **RFC ID**: RFC-000
- **Title**: Introduce Legacy Token-Based Authentication
- **Author(s)**: John Doe (Iris)
- **Created Date**: 2023-03-15
- **Status**: Deprecated
- **Version**: v1.2
- **Squads**: Iris

---

## 1. Motivation
At the time, we needed a simple token-based authentication system to bootstrap our services quickly.

---

## 2. Background / Context
Originally, no unified authentication existed.  
This RFC introduced a stop-gap token solution.  

---

## 3. Proposal
Use a custom token header (`X-Auth-Token`) validated by backend services.  

---

## 4. Alternatives Considered
- OAuth2 → rejected due to implementation complexity at that time.  
- API keys → rejected because tokens provided finer control.  

---

## 5. Impact Analysis
- Quick to implement.  
- Did not scale well for multi-tenant apps.  
- No support for federated identity.  

---

## 6. Risks & Mitigations
- Security weaknesses → mitigated via short TTL tokens.  

---

## 7. Rollout & Monitoring
- Deployed in 2023 across Iris services.  
- Eventually replaced by OAuth2 (see RFC-010).  

---

## 8. Changelog
- v1.0 – Initial draft  
- v1.1 – Added token TTL  
- v1.2 – Marked as Deprecated  

---

## 9. References
- Successor: [RFC-010: OAuth2 Authentication](../RFC-010-oauth2-auth/RFC-010-oauth2-auth.md)  
- Notes: [`notes/decisions-log.md`](./notes/decisions-log.md)  
