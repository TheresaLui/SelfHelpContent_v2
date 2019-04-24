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

# Too many redirects error

We ran the below diagnostic check to verify whether the cookie-based session affinity feature has been enabled or not on your resource <!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->

## **Diagnostic checks executed**

Check for <!--$SessionAffinityNotConfiguredDisplayName-->[SessionAffinityNotConfiguredDisplayName]<!--/$SessionAffinityNotConfiguredDisplayName--> - <!--$SessionAffinityNotConfiguredCheckStatusName-->[SessionAffinityNotConfiguredCheckStatusName]<!--/$SessionAffinityNotConfiguredCheckStatusName-->

## **Recommended Steps**

- If the Diagnostic check above fails, it implies that the feature has not been configure on the Application Gateway. You can enable cookie-based session affinity by enabling the **Cookie based affinity** switch in the [HTTP Settings](https://docs.microsoft.com/azure/application-gateway/configuration-overview#http-settings) associated with the required backend pool. 
- If the Diagnostic check above is successful, then check whether your application cannot handle cookie-based affinity or not. If the backend application cannot handle cookie-based affinity, then Application Gateway will not be able to support session affinity. This is because the Application Gateway can perform session affinity only by using a cookie. As a workaround, you can consider using an external or internal azure load balancer or another third-party solution.
- If you access the Application Gateway by using a short name URL in Internet Explorer, for example: [http://website](http://website/) , the request is may bounce between back-end servers. 
  - [Perform these steps to root-case the issue](https://docs.microsoft.com/azure/application-gateway/how-to-troubleshoot-application-gateway-session-affinity-issues#symptom).
  - To fix this issue, you should access the Application Gateway by using a FQDN. For example, use [http://website.com](https://website.com/) or [http://appgw.website.com](http://appgw.website.com/).