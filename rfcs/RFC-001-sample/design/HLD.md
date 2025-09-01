# High-Level Design (HLD)

- Redis cluster introduced between API service and database.  
- SDK modified to check cache before DB call.  
- Foundry handles cache invalidation on writes.  

Diagram: see [`../diagrams/cache-flow.png`](../diagrams/README.md).
