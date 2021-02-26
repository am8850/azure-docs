# Azure API Management

## Beginner

Topics:

- Introduction to API Management
- API Management in Microservices architectures
- Networking (off, external, internal)
  - Required ports
- Hard requirements
  -	Only resource on subnet
  -	/29 minimum size of subnet
  -	Service Endpoints need to be enabled for Azure Sql, Azure Storage, Azure EventHub, and Azure ServiceBus(At least to Azure SQL Database and Storage Accounts(Table and Blob)
- API definitions
- Understanding the request pipeline
- Products
- Subscriptions
- Users
- Developer portal
- Monitoring:
  - ApplicationInsights
- Demo:
  - Deploying an API Management Instance and discussing an API

## Intermediate

Topics:

- External Cache
- Policies
- Oauth and OpenID

## Advanced

Topics:

- [Application Gateway and API Management](https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-integrate-internal-vnet-appgateway#:~:text=Integrating%20Application%20Gateway%20with%20API%20Management%20provides%20the,as%20a%20frontend%20to%20your%20API%20Management%20instance.)
- [Application Gateway and FrontDoor](https://azure.microsoft.com/en-us/resources/templates/201-front-door-api-management/)
- Monetization using subscription keys
- DevOps:
  - APIM DevOpts tools
  - Deploying an API using the DevOPs

## Other Topics

### Internal VNET: Public Endpoints
 
[A Public address is required for managing configuration on port 3443](https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-ip-addresses#ip-addresses-of-api-management-service-in-vnet)
 
NSG quick start for Inbound/Outbound rules for Internal VNET. azure-quickstart-templates/azuredeploy.json at master · Azure/azure-quickstart-templates (github.com)
 
### Internal VNET: Force Tunneling
 
If force tunneling is implemented through a UDR, Control Plane IP Addresses need to be routed to the "Internet". 
microsoft/HighSecurityAPIM: Secure VNET Injection of APIM Surviving Force-Tunneling (github.com)
 
### Isolated Tier
 
[Satisfy the DoD IL5 isolation requirement](https://docs.microsoft.com/en-us/azure/api-management/upgrade-and-scale#compute-isolation)
 
 
### Troubleshooting
 
Timeout issues with updating an API. Navigate to global policy for <forward-request> under the “All APIs”.

(https://docs.microsoft.com/en-us/azure/api-management/api-management-advanced-policies#ForwardRequest)
  
<forward-request timeout policy>
 
#### VS Code 

[Debugging Policies](https://docs.microsoft.com/en-us/azure/api-management/api-management-debug-policies)
 

