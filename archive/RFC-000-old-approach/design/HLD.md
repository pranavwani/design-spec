# High-Level Design (Legacy Auth)

- Clients attach `X-Auth-Token` to every request.  
- Backend validates token against in-memory store.  
- Tokens issued via bootstrap service.  
