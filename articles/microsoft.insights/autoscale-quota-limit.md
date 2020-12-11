<properties
    pageTitle="I hit quota limits in Autoscale"
    description="I hit quota limits in Autoscale"
    service="microsoft.insights"
    resource="components"
    authors="shilpasharmaAM"
    ms.author="shilsha"
    displayOrder="2"
    articleId="metrics-autoscalequotalimits"
    selfHelpType="generic"
    supportTopicIds="32684749"
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-autoscalequotalimits -->

You can use **Activity Log** to verify results of autoscale actions to confirm that quota has indeed been exhausted which prevents further scaling operations.

## **Recommended Steps**

1. Open **Activity Logs** and Track if there is a failure message associated with unavailability of capacity.
1. Reach out to the Azure customer service to request for additional capacity. Once the resources are made available, autoscale automatically resumes the scaling operation.


## **Recommended Documents**

* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)
* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Best practices for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices)