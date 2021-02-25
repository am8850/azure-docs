# Azure App Service (Window/Linux/Containers)

## Beginner

Objectives:

- Understand what is an App Service
- Understand to how to select service plan
- Understand how to scale and App Service plan
- Understand how to deploy code to an App Service

Topics:

- Introduction to App Services
- Service plan
- Choosing an App Service
- Options for deploying code
- Scaling up/down and out/in
> **Tip:** A service plan can host multiple apps. What scales if the plan. If you need more scalability flexibility for a given app, consider separating it to its own service plan.
- Deployment slots
> **Tip:** You could deploy an app to a pre-prod, test it, and the swap from pre-prod to prod. This works with a DNS replacement.
- Application settings in configuration
> **Tip:** Consider using Keyvault to store your secrets or manage identities to complety skip having to deploy secrets.
- Monitoring:
  - ApplicationInsights
- Deploying a SPA application (Storage account)
- Demo:
  - Deploying an .Net Core/Node app to an App Service

## Intermediate

Objetives:

- Understand how to deploy containers
- Understand some performance differences.
- Understand networking capabilities in premium services.

Topics:

- Custom nost names and TLS
> **Tip:** you will need to obtain a PFX certificate and have access to configure DNS entries.
- Deploying a containers
- Java Apps on Tomcat
  - How are WAR file restored on App Service
  > **Tip:** Tomcat can host many apps, but when an app is deployed to App Services, it is expanded at root level. For example, if your app was access by going to http://server/app/index.jsp in App Service the same app would be available at: https://appservice.net/index.jsp.
- Perforamnce:
  - Differences between ZipDeploy (local) and WebDeploy (NFS)
- Networking:
  - Restrictions
  - Application Gateway in WAF mode
- Performance
  - Caching (i.e. with Redis cache)
- Security:
  - AAD integration
  - Managed Identities

## Advanced

Objectives:

- Understand the value of App Service Environments
- Understand the networking features in premium tiers of App Services
- DevOPS CI/CD to deploy an app to App Service with configuration secrets

Topics:

- App Service Environments
  - Hardware and network isolation (Good for very strick compliance such as banking and Federal)
- Networking:
  - Premium plans and accessing resources on a VNET or with Private Link
  - Connecting to on-prem resources with Hybrid connections
- DevOps:
  - Keyvault
  - Deploying an application to App Service
