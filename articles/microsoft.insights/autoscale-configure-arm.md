<properties
    pageTitle="I can’t configure autoscale using Azure Resource Manager (ARM) template"
    description="Issues with using Azure Resource Manager (ARM) template to configure autoscale"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="autoscale-configure-arm"
    selfHelpType="generic"
    supportTopicIds="32683739"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-configure-arm -->

You can use Azure Monitor autoscale with Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, and API Management services. Follow the recommended steps if you are experiencing an issue with using Azure Resource Manager (ARM) template to configure autoscale rules.

## **Recommended Steps**

1. Verify that you are configuring autoscale for a resource type that supports autoscale (Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, or API Management services)
1. Review the walkthrough that explains [how to configure autoscale using Azure ARM Templates](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-virtual-machine-scale-sets#walkthrough)
1. Review the [troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)

## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Best practices for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)
