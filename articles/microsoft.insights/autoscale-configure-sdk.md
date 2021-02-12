<properties
    pageTitle="I can’t configure autoscale using SDK"
    description="Issues configuring autoscale using SDK"
    service="microsoft.insights"
    resource="components"
    authors="shilpasharmaAM"
    ms.author="shilsha"
    displayOrder="2"
    articleId="autoscale-configure-sdk"
    selfHelpType="generic"
    supportTopicIds="32683744"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-configure-sdk -->

You can use Azure Monitor autoscale with Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, and API Management services. Follow the recommended steps if you are experiencing an issue configuring autoscale using SDK.

## **Recommended Steps**

1. Verify that you are configuring autoscale for a resource type that supports autoscale (Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, or API Management services)
1. You can use Fluent API libraries to build Azure .Net SDK. [Review the reference](https://docs.microsoft.com/dotnet/api/overview/azure/monitor?view=azure-dotnet)
1. You can browse autoscale related code samples [here](https://docs.microsoft.com/samples/browse/?products=azure&term=autoscale) and use the guidelines to configure autoscale via SDK.

## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Best practices for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)