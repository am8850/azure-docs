# AKS

## Beginner

Session objetives:
- Basic understanding of kubernetes architecture
- Basic kubernetes network understanding
- Basic understanding of AKS
- Provisioning an AKS cluster from CLI
- Basic understanding of deploying a deployment and a service to AKS

Session topics

- [Kubernetes architecture](https://docs.microsoft.com/en-us/azure/aks/concepts-clusters-workloads)
  - Master node, worker node, pod, pod networking
  - NodePort, ClusterIP
  - Other services (API server, ETCD, scheduler, etc.)
- AKS (Azure's implementation of Kubernetes)
  - Networking: 
    - Private and Public cluster
    > **Tip:** Selecting a public or private cluster is the first importante decision. In a private cluster, the control plane or API server has internal IP addresses 
    - Kubnet vs ACI
    > **Tip:** ACI is recommended, but you may select kubenet when you have exhausted IP in the network where the cluster will be delopyed. 
    - NodePort
    - LoadBalancer (public/private with annotations)
    - Deployments and Services    
    - [Network policies](https://docs.microsoft.com/en-us/azure/aks/use-network-policies)
    > **Tip:** Namespaces do not provide network isolation. Use network policies instead.
  - Monitoring:
    - Azure Container Monitoring
    - Application Insights in containers
- Demo:
  - Provisioning a cluster
```bash
az aks create \
    --resource-group <private-cluster-resource-group> \
    --name <private-cluster-name> \
    --load-balancer-sku standard \
    --enable-private-cluster \
    --network-plugin azure \
    --vnet-subnet-id <subnet-id> \
    --docker-bridge-address 172.17.0.1/16 \
    --dns-service-ip 10.2.0.10 \
    --service-cidr 10.2.0.0/24 
```
  - Getting credentials
  - Basic kubectl commands
  > **Tip:** [This site](https://github.com/dgkanatsios/CKAD-exercises) provides good excersises on using the kubectl command
  - Deploy a deployment and a service

- Links:

  - [Walkthrough](https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough)

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
