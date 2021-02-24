# AKS

## Beginner

- Containerizing an app using docker to docker hub
- Azure container registry
- Kubernetes architecture
  - Master node, worker node, pod, pod networking
  - NodePort, ClusterIP
  - Other services (API server, ETCD, scheduler, etc.)
- AKS (Azure's implementation of Kubernetes)
  - Networking: 
    - Private and Public master node
    - Kubnet vs ACI
    - LoadBalancer (public/private)
    - Deployments and Services    
    - [Network policies](https://docs.microsoft.com/en-us/azure/aks/use-network-policies)
  - Scaling:
    - Pod and node scaling
  - Policies
  - RBAC and AAD
  - Monitoring:
    - Azure Container Monitoring
    - Application Insights in containers
- Deploying a solution to AKS
    - Basic kubectl commands

## Intermediate

- AKS
  - Security: 
    - Pod identities
  - Ingress controllers
  - Secret management
  - ConfigMaps
  - Persistance
- ACR
  - Premium features of ACR
- Nodepool upgrade and maintenance
- Monitoring
  - Premetheus and Grafana
- Helm, Traefik and other CNCF graduated projects

## Advanced

- AKS
  - Detailed security recommendations
- Microservices Architecture with AKS
  - Decoupling, messanging
  - DAPR
