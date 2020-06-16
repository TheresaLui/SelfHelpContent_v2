<properties 
    pageTitle="End-to-end transaction details data is incorrect or incomplete"
    description="End-to-end transaction details data is incorrect or incomplete"
    service="microsoft.insights"
    resource="components"
    authors="osvaldorosado"
    ms.author="osrosado"
    articleId="insights-txndetails-incorrect"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729585,32729584,32729583"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	 ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# End-to-end transaction details data is incorrect or incomplete

## **Recommended Steps**

If you can see data from your services in Application Insights, but aren't getting a complete view in End-to-end transaction details, try the following steps:

1. Make sure you have read access to every Application Insights resource used in your transaction. See [Roles Overview](https://docs.microsoft.com/azure/azure-monitor/app/resources-roles-access-control) for information on access control in Application Insights.
2. Make sure you're using an officially supported SDK. Unsupported/community SDKs might not support correlation. Refer to [this article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs.
3. Upgrade all components to the latest SDK version
   - If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/azure/azure-functions/functions-versions)
5. If some transactions are complete, but not all, [double-check your sampling settings](https://docs.microsoft.com/azure/application-insights/app-insights-sampling). By default, adaptive sampling generally only occurs at higher traffic volumes
   - If sampling is in effect but cannot be reduced, make sure to select the **"Suggested"** result when opening a transaction from Performance or Failures. The suggested transaction is least likely to be impacted by sampling.
6. If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies). If not, you can still track it manually with a [track dependency call](https://docs.microsoft.com/azure/application-insights/app-insights-api-custom-events-metrics#trackdependency).