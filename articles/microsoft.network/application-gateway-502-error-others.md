<properties
    pageTitle="Application Gateway other issues"
    description="Application Gateway other issues"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="32"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f2"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783370"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway other issues

Use the following steps to resolve "502 Bad Gateway" errors from Application Gateway when the back-end server status is otherwise healthy.


## **Recommended Steps**

* If you use Application Gateway v1 (Standard or WAF), the request may be timing out at your back-end server. This means that your back-end server took more time to respond to the request than what's configured in the request timeout field of the HTTP settings. Increase the timeout in the respective HTTP settings, or determine why your back-end server is taking longer than expected to respond. Learn more about [troubleshooting request timeouts](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#request-time-out).

- If your Application Gateway utilization is high, you might receive 502 errors intermittently. This usually happens during peak traffic and if the gateway is not scaled appropriately to handle the traffic. Learn how scaling and alerts can help you [support high traffic in Application Gateway](https://docs.microsoft.com/azure/application-gateway/high-traffic-support).

## **Recommended Documents**

- [Troubleshoot bad gateway errors in Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
- [Troubleshoot back-end health issues in Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting)
- [Azure Application Gateway Resource Health overview](https://docs.microsoft.com/azure/application-gateway/resource-health-overview)
