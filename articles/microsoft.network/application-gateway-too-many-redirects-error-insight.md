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

We ran the below diagnostic check on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->**. Check the status of the diagnostic check and if it has failed, use the recommended steps to troubleshoot the issue.

## **Diagnostic checks executed**

* Check for <!--$RedirectionLoopDisplayName-->[RedirectionLoopDisplayName]<!--/$RedirectionLoopDisplayName--> - <!--$RedirectionLoopCheckStatus-->[RedirectionLoopCheckStatus]<!--/$RedirectionLoopCheckStatus-->

## **Recommended Steps**

1. If the Diagnostic check above fails, it implies that the Application Gateway is configured with SSL offload but the backend server can accept only HTTPS requests. Since the request from the Application Gateway to the backend is not encrypted, the backend redirects the client to use only HTTPS. This results in a redirection loop. You can also verify this by analyzing the [access logs](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#access-log).

    To resolve this, you can either modify the backend to accept HTTP requests or [configure the Application Gateway to have end-to-end SSL termination](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal). 

2. If the diagnostic check status succeeds, then you need to check if the backend has a redirection loop. You can verify this by bypassing the Application Gateway to directly access the backend. If you still observe the same error, then the issue is with the backend and not with the Application Gateway.
