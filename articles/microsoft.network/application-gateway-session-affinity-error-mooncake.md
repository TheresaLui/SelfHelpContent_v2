<properties 
    pageTitle="Session affinity issues"
    description="Session affinity issues with Azure Application Gateway"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="24"
	selfHelpType="resource"
    articleId="application-gateway-session-affinity-error-mooncake"
	resourceTags=""
	productPesIds=""
    supportTopicIds=""
    cloudEnvironments="MoonCake"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Session affinity issues with Application Gateway

## **Recommended Steps**

- Check whether cookie-based session affinity has been enabled. You can enable cookie-based session affinity by enabling the **Cookie based affinity** switch in the [HTTP Settings](https://docs.azure.cn/application-gateway/configuration-overview#http-settings) associated with the required backend pool. 
- Check whether your application can handle cookie-based affinity. If the backend application cannot handle cookie-based affinity, then Application Gateway will not be able to support session affinity. This is because the Application Gateway can perform session affinity only by using a cookie. As a workaround, you can consider using an external or internal azure load balancer or another third-party solution.
- If you access the Application Gateway by using a short name URL in Internet Explorer, for example: `http://contoso` , the request may bounce between back-end servers
- [Perform these steps to root-cause the issue](https://docs.azure.cn/application-gateway/how-to-troubleshoot-application-gateway-session-affinity-issues#symptom)
- To fix this issue, you should access the Application Gateway by using a FQDN. For example, use `http://contoso.com` or `http://appgw.contoso.com`.

## **Recommended Documents**

* [Troubleshoot session affinity issues with Application Gateway](https://docs.azure.cn/application-gateway/how-to-troubleshoot-application-gateway-session-affinity-issues)
