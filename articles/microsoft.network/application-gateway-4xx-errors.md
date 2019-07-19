<properties
    pageTitle="I'm encountering 4xx client error"
    description="400 Bad Request, 403 Forbidden, 404 Not Found"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="22"
	selfHelpType="resource"
    articleId="application-gateway-4xx-error"
 	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32639113"
    cloudEnvironments="public"
 />

# 4xx client error
4xx errors can occur either due to an issue at the backend application or due to incorrect configuration of Application Gateway. Use the below instructions to troubleshoot the problem.

## **Recommended Steps**

- **Listener configuration issue:** You can get a 404 error, when the multi-site listener that is matching the IP, port and protocol of the request does not match the host name in the request. Ensure that the host value entered in the listener configuration is the same as the host header in the client request.
- **WAF issue**: You can get a 403 error when the Web Application Firewall (WAF) is blocking the request. Analyze the [WAF logs](https://docs.microsoft.com/azure/application-gateway/waf-overview#logging) to evaluate whether the WAF is blocking the request
- **Backend application issue**: Bypass the Application Gateway to directly access the backend server. If the backend server still returns the same 4xx error, then the issue is with the backend and not the Application Gateway.

## **Recommended Documents**

Verify the HTTP response code that Application Gateway received from the backend by viewing the *SERVER-STATUS* value in *RequestQuery* field of [access logs](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#diagnostic-logging). If the response code is 4xx, then it's an issue with your backend and not the application gateway.