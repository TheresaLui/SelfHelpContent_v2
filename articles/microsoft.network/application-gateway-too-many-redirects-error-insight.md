<properties 
    pageTitle="I'm encountering too many redirects"
    description="Too many redirects"
    infoBubbleText="Diagnostic checks to root-cauase the too-many redirects issue"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-too-many-redirects-error-insight"
    diagnosticScenario="ApplicationGatewayTooManyRedirectsError"
    supportTopicIds="32639115"
	productPesIds="15922"
    cloudEnvironments="public"
 />

# Too many redirects error

We ran several diagnostics on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->** and have found the below issues because of which you are encountering too many redirects.

## **Issues identified**

 <!--$failedCheckList-->[failedChecklist]<!--/$failedCheckList-->

## **Recommended Steps**

if the diagnostics above cannot identify any issues, then you need to check if the backend has a redirection loop. You can verify this by bypassing the Application Gateway to directly access the backend. If you still observe the same error, then the issue is with the backend and not with the Application Gateway.