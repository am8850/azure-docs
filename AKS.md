# AKS

## Beginner

Session objetives:
- Basic understanding of kubernetes architecture
- Basic kubernetes network understanding
- Basic understanding of AKS
- Basic understanding of deploying a deployment and a services

Session topics

- [Kubernetes architecture](https://docs.microsoft.com/en-us/azure/aks/concepts-clusters-workloads)
  - Master node, worker node, pod, pod networking
  - NodePort, ClusterIP
  - Other services (API server, ETCD, scheduler, etc.)
- AKS (Azure's implementation of Kubernetes)
  - Networking: 
    - Private and Public master node
    - Kubnet vs ACI
    - LoadBalancer (public/private with annotations)
    - Deployments and Services    
    - [Network policies](https://docs.microsoft.com/en-us/azure/aks/use-network-policies)
  - Monitoring:
    - Azure Container Monitoring
    - Application Insights in containers
- Deploying a solution to AKS
    - Basic kubectl commands to deploy a deployment and a service

## Intermediate

- AKS
  - Scaling:
    - Pod and node scaling 
  - Security: 
    - AAD integration
    - Pod identities
  - Ingress controllers (AppGw, NGINX, Traefik)
  - Secret management
  - ConfigMaps
  - Persistance
- ACR
  - AKS and ACR integration
  - Premium features of ACR
- Nodepool upgrade and maintenance
- Monitoring
  - Premetheus and Grafana
- Helm and other CNCF graduated projects

## Advanced

- AKS
  - Detailed security recommendations
  - Private cluster networking
- Microservices Architecture with AKS
  - Decoupling, messanging
  - DAPR
- DevOPS
  - Deploying a solution using GitOps
- Introduction to Service Mesh
