<properties
    pageTitle="I'm encountering 4xx client error"
    description="400 Bad Request, 403 Forbidden, 404 Not Found"
    infoBubbleText="Common solution article for instructions on how to troubleshoot 4xx errors with Application Gateway."
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-4xx-error"
    diagnosticScenario="ApplicationGateway4xxClientError"
    supportTopicIds=""
    cloudEnvironments="public"
 />

# 4xx client error
<!--/issueDescription-->
I'm encountering 4xx client error.
<!--/issueDescription-->

## **Recommended Steps**

4xx errors are usually client side errors and can occur due to one or more of the following reasons:

- **Backend Server returns 4xx error**: You can identify this by bypassing the Application Gateway to directly access the server. If the backend server still returns the same 4xx error, then the issue is with the backend and not the Application Gateway.
- **No listener to accept the request**:  This can happen when Application Gateway does not have a rule with basic listener and the hostname of the request does not match with any multi-site listeners. Check the configuration of the Application Gateway and add a listener to accept the request.
- 403 error due to Web Application Firewall (WAF) blocking the request

## **Recommended Documents**

* Analyze the [WAF logs](https://docs.microsoft.com/azure/application-gateway/waf-overview#logging) to evaluate whether the WAF is blocking the request
