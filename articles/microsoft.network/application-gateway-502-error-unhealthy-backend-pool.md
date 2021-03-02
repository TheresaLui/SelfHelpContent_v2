<properties
    pageTitle="Unhealthy back-end pool"
    description="Unhealthy back-end pool"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="30"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f0"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783371"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Unhealthy back-end pool
When all of the servers in a back-end pool are unhealthy, Application Gateway has no healthy servers to forward client requests to. 

These issues can stem from the health probe configuration in Application Gateway or your back-end server, which fails to give a healthy response. In this case, the clients will receive a "502 Bad Gateway" error to signify that no active servers are available to accept the requests.

## **Recommended Steps**

To troubleshoot 502 Bad Gateway errors, open the **Backend health** blade and follow these steps:

[Open Backend Health](button-data-blade:Microsoft_Azure_HybridNetworking.ApplicationGatewayBackendHealthGridBlade.id.$resourceId)

1. In the **Backend health blade**, check the error message for an unhealthy server
2. Check the error message in the **Details** column
3. Visit [Back-end health troubleshooting](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#back-end-health) to learn about troubleshooting steps for each error message

Alternatively, you can check the detailed error message by using Azure PowerShell, CLI, or REST API. For more information, see [Back-end health and diagnostic logs for Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#back-end-health).

## **Recommended Documents**

- [Troubleshoot bad gateway (502) errors in Azure Application Gateway](https://support.microsoft.com/help/4504111)
- [Learn how to troubleshoot bad gateway (502) errors in Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
- [Troubleshoot back-end health issues in Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting)
