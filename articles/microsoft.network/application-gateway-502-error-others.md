<properties
    pageTitle="Application Gateway other issues"
    description="Application Gateway other issues"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f2"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783370"
    cloudEnvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
 />

# Application Gateway other issues

## **Recommended Steps**

If the health status of the back-end server is healthy, but if Application Gateway returns 502 Bad Gateway error, it could be due to one of the following reasons:

- If you are using v1 SKU of Application Gateway (Standard or WAF), then 502 error can also occur due to the request getting timed out at your back-end server, which means that your back-end server took longer time to respond to the request than what's configured in the request timeout field of HTTP settings. In this case, increase the timeout in the respective HTTP settings or check why your back-end server is taking longer than expected to respond. See [this article](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#request-time-out) to learn more about troubleshooting request timeouts.
- If your Application Gateway's utilization is high, you might receive 502 errors intermittently. This usually happens during peak traffic and if the gateway is not scaled appropriately to handle the traffic. See [Application Gateway high traffic support](https://docs.microsoft.com/azure/application-gateway/high-traffic-support) to learn more about Application Gateway scaling and alerts.

## **Recommended Documents**

- [Troubleshoot bad gateway errors in Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
- [Troubleshoot backend health issues in Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting)
- [Azure Application Gateway Resource Health overview](https://docs.microsoft.com/azure/application-gateway/resource-health-overview)
