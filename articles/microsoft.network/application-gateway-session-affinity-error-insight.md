<properties 
    pageTitle="Session affinity issues"
    description="Session affinity issues with Azure Application Gateway"
    infoBubbleText="Diagnostic checks to root-cauase session affinity issue"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-session-affinity-insight"
    diagnosticScenario="ApplicationGatewaySessionAffinity"
    supportTopicIds=""
    cloudEnvironments="public"
 />

# Session affinity issues with Application Gateway
We ran several diagnostics on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->** and have found the below issues because of which you are encountering session affinity issues.

## **Issues identified**

 <!--$failedCheckList-->[failedChecklist]<!--/$failedCheckList-->

## **Recommended Steps**

The following are other issues which cannot be identified by the diagnostics but can result in session affinity issues:

- Check whether your application can handle cookie-based affinity or not. If the backend application cannot handle cookie-based affinity, then Application Gateway will not be able to support session affinity. This is because the Application Gateway can perform session affinity only by using a cookie. As a workaround, you can consider using an external or internal azure load balancer or another third-party solution.
- If you access the Application Gateway by using a short name URL in Internet Explorer, for example: `http://website`, the request may bounce between back-end servers
  - [Perform these steps to locate the root cause of the issue](https://docs.microsoft.com/azure/application-gateway/how-to-troubleshoot-application-gateway-session-affinity-issues#symptom)
  - To fix this issue, you should access the Application Gateway by using a FQDN. For example, use `http://website.com` or `http://appgw.website.com`

