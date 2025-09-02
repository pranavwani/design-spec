# Deployment / Rollout

- Deploy Redis via Helm chart in k8s.  
- Rollout gradually: 10% → 50% → 100%.  
- Monitor DB load, Redis CPU/memory.  
- Rollback: disable feature flag and bypass cache.  
