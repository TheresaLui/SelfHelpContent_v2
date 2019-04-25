<properties 
    pageTitle="I'm encountering too many redirects"
    description="Too many redirects"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-too-many-redirects-error"
    diagnosticScenario="ApplicationGatewayTooManyRedirectsError"
    supportTopicIds="32639115"
    cloudEnvironments="public"
 />

# Too many redirects error

## **Recommended Steps**

1. Check if the backend has a redirection loop. You can verify this by bypassing the Application Gateway to directly access the backend. If you still observe the same error, then the issue is with the backend and not with the Application Gateway.

2. If the Application Gateway is configured with SSL offload  but backend server can accept only HTTPS requests, then this can lead to redirection loop. This is because since the request from the Application Gateway to the backend is not encrypted, the backend redirects the client to use only HTTPS. You can also verify this by analyzing the [access logs](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#access-log).

   To resolve this, you can either modify the backend to accept  HTTP requests or [configure the Application Gateway to have end-to-end SSL termination](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal). 