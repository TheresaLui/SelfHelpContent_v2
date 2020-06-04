<properties
    pageTitle="Autoscale action too long or never completed"
    description="Troubleshooting autoscale actions that too long or never completed"
    service="microsoft.insights"
    resource="components"
    authors="shilpasharmaAM"
    ms.author="shilsha"
    displayOrder="2"
    articleId="autoscale-action-nevercompleted"
    selfHelpType="generic"
    supportTopicIds="32683736"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-action-nevercompleted -->

You can use **Activity Log** to verify results of autoscale actions and review any errors. Further to that it has been observed that main cause for autoscale taking too long, or for autoscale operation not completing is because the capacity has been exhausted and additional resources are not available.

## **Recommended Steps**

1. Confirm that the scale actions did infact start. Open **Activity Logs** and apply filter to the subscription your autoscale setting is in. Then choose **Autoscale** as the event category, and review the messages.
1. Track if there is a failure message associated with unavailability of capacity.
1. Reach out to the Azure customer service to request for additional capacity. Once the resources are made available, autoscale automatically resumes the scaling operation.
1. If you haven't already done it yet, consider setting up email notifications to receive notifications when an autoscale operation is unable to start or complete. Review [how to configure autoscale notifications](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-webhook-email)

## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Best practices for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)