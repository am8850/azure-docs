# AKS

## Beginner

Session objetives:
- Basic understanding of kubernetes architecture
- Basic kubernetes network understanding
- Basic understanding of AKS
- Provisioning an AKS cluster from a portal and from CLI
- Basic understanding of deploying a deployment and a service to AKS

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
- Demo:
  - Provisioning a cluster
    - Getting credentials
  - Basic kubectl commands
  - Deploy a deployment and a service

## Intermediate

Session objectives:

- Understand scaling capabilities in AKS
- Undersntad more security options with AAD and Pod Identities
- Understand what ingress controllers are and how they can be used
- Understand how to leverage Helm
- Understand more monitoring options with Prometheus


Topics:

- AKS
  - Scaling:
    - Pod and node scaling 
  - Security: 
    - AAD integration
    - Pod identities
  - Ingress controllers
    - Path based routing
  - Secret management
  - ConfigMaps
  - Persistance
- ACR
  - AKS and ACR integration
  - Premium features of ACR
- Nodepool upgrade and maintenance
- Helm and other CNCF graduated projects
- Monitoring
  - Premetheus and Grafana


## Advanced

Session bjectives:

- Understand more 

Topics:

- AKS
  - Detailed security recommendations
  - Private cluster networking
- Microservices Architecture with AKS
  - Decoupling, messanging
  - DAPR
- DevOPS
  - Deploying a solution using GitOps
- Introduction to Service Mesh
