<properties
    pageTitle="Unhealthy back-end pool"
    description="Unhealthy back-end pool"
    ms.author="mariliu"
    displayOrder=""
    articleId="e5e52652-4b63-4897-a4c5-90c0fb72c90f"
    selfHelpType="Apollo"
    supportTopicIds="4a2660bb-e876-33ba-052c-0cd103bc72d3"
    productPesIds="15922"
    cloudEnvironments="public"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Unhealthy back-end pool
<!--/issueDescription-->
When all of the servers in a back-end pool are unhealthy, Application Gateway has no healthy servers to forward client requests to. In this case, the clients will receive a "502 Bad Gateway" error to signify that no active servers are available to accept the requests.
<!--/issueDescription-->

:::Section Insights:::
## **Diagnostics**
<Insight>
	<symptomId>AppGw502AzurePortalInsight</symptomId>
	<executionText>We are running a few checks on your resource</executionText>
	<timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
	<noResultText>This check completed without reporting any problems</noResultText>
    <failedText>We ran into an issue and could not complete this check</failedText> 
	<maxInsightCount>1</maxInsightCount>
	<additionalInputsReq>true</additionalInputsReq>
</Insight>
<br>

## **Recommended Steps**

If you receive 502 Bad Gateway error due to unhealthy servers in your back-end pool, troubleshoot the cause using the following steps:

1. In the **Backend health** blade, check the error message for an unhealthy server. Alternatively, you can check the detailed error message by using Azure PowerShell, CLI, or REST API. For more information, see [Back-end health and diagnostic logs for Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#back-end-health).
2. Based on the error message in the **Details** column, you can troubleshoot the issue and fix the root cause for the probe to be marked unhealthy. The issue could stem from the health probe configuration in Application Gateway or your back-end server, which fails to give a healthy response. See [Back-end health troubleshooting](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#back-end-health) to learn about troubleshooting steps for each error message.

## **Recommended Documents**

- [Troubleshoot bad gateway (502) errors in Azure Application Gateway](https://support.microsoft.com/help/4504111).
- [Learn how to troubleshoot bad gateway (502) errors in Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502).
- [Troubleshoot back-end health issues in Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting).
