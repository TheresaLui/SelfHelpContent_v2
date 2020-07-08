<properties
    pageTitle="I didn't receive autoscale notifications"
    description="Issues with autoscale notifications"
    service="microsoft.insights"
    resource="components"
    authors="ssharma"
    ms.author="shilpasharmaAM"
    displayOrder="2"
    articleId="autoscale-configure-notifications"
    selfHelpType="generic"
    supportTopicIds="32683745"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-configure-notifications -->

You can use Azure Monitor autoscale with Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, and API Management services. Follow the recommended steps if you are experiencing an issue with setting up and receiving autoscale notifications.

## **Recommended Steps**

1. Verify that you are configuring autoscale for a resource type that supports autoscale (Virtual Machine Scale Sets, Cloud Services, App Service - Web Apps, or API Management services)
1. Review the walkthrough that explains [how to configure autoscale notifications](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-webhook-email)
1. Review the [best practices on setting up autoscale notifications](https://docs.microsoft.com/Azure/azure-monitor/platform/autoscale-best-practices#configure-autoscale-notifications)
1. If you did not receive a notification as expected, check the validity of the email or distribution list added for autoscale notification. Further, revalidate user rights, especially with email distribution lists.


## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Best practices for autoscale](https://docs.microsoft.com/Azure/azure-monitor/platform/autoscale-best-practices)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)
