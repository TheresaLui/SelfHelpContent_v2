<properties
    pageTitle="I can’t configure autoscale using Azure CLI"
    description="Issues with using Azure CLI to configure autoscale"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="autoscale-configure-cli"
    selfHelpType="generic"
    supportTopicIds="32683740"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-configure-cli -->

You can use Azure Monitor autoscale with Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, and API Management services. Follow the recommended steps if you are experiencing an issue with using Azure CLI to configure autoscale rules.

## **Recommended Steps**

1. Verify that you are configuring autoscale for a resource type that supports autoscale (Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, or API Management services)
1. Review the walkthrough that explains [how to configure autoscale using Azure CLI](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-autoscale-cli)
1. Check the syntax of [Azure Monitor CLI commands and parameters](https://docs.microsoft.com/cli/azure/monitor/autoscale) that you can use with Azure autoscale
1. Review the [troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)

## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Get started with Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)
