<properties
    pageTitle="I'm encountering 4xx client error"
    description="400 Bad Request, 403 Forbidden, 404 Not Found"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="19"
	selfHelpType="resource"
    articleId="application-gateway-4xx-errors-mooncake"
 	resourceTags=""
	productPesIds=""
    supportTopicIds=""
    cloudEnvironments="MoonCake"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# 4xx client error
4xx errors can occur either due to an issue at the backend application or due to incorrect configuration of Application Gateway. Use the below instructions to troubleshoot the problem.

## **Recommended Steps**

1. Bypass the Application Gateway to directly access the backend server. If the backend server still returns the same 4xx error, then the issue is with the backend and not the Application Gateway. You can also verify this by observing the HTTP response code that Application Gateway received from the backend by viewing the *SERVER-STATUS* value in *RequestQuery* field of [access logs](https://docs.azure.cn/application-gateway/application-gateway-diagnostics#diagnostic-logging). 

   If the response code from the backend is verified to be 4xx, then it's an issue with your backend and not the application gateway. If the response from the backend is verified to be valid, then follow the steps below to troubleshoot.

2. If you are getting a 404 error, then it could be a listener configuration issue. This could happen when the multi-site listener that is matching the IP, port and protocol of the request does not match the host name in the request. Ensure that the host value entered in the listener configuration is the same as the host header in the client request.
3. If you are getting a 403 error and using Web Application Firewall (WAF) SKU of the Application Gateway, then this behavior can happen if WAF is blocking the request. Analyze the [WAF logs](https://docs.azure.cn/application-gateway/waf-overview#logging) to evaluate whether the 403 error is due to WAF blocking the request.