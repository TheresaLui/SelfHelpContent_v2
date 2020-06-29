<properties
     pageTitle="I cannot find some of my VM metrics in Azure Metrics Explorer"
    description="I cannot find some of my VM metrics in Azure Metrics Explorer"
    infoBubbleText="Here are some things to help with metrics explorer"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-os-not-supported"
    productPesIds="17081"
    supportTopicIds="32738515"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

# I see a message that my operating system may not be supported

## **Recommended Steps**

When you enable monitoring on your Azure VM or VM scale set you can choose to do so through our onboarding process in the portal.

In this UI, you may see a message that the operating system on your VM *may* not be supported.

This message is displayed when the OS image you are using has limited metadata defining the operating system that will is being used on the VM image.  In this case, we don't have enough details from the VM image to determine if we support the operating system and display this message and let you proceed with installation.

If we can detect that the OS on the VM is not supported, we display a different message that looks similar to the following:

![OS Not Supported](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-ossupported/os-not-supported-01.png?branch=pr-en-us-115799)

For a list of our currently operating systems supported please refer to our [deployment documentation](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-overview#supported-operating-systems).

If your operating system is not supported, an attempt to install the two extensions on the VM will fail to install properly and should be removed.
