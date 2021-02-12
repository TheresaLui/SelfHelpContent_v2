<properties
       pageTitle="I see a message that the Azure agent needs to be upgraded"
    description="I see a message that the Azure agent needs to be upgraded"
    infoBubbleText="Here are some things to help with updating the azure agent"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-agent-upgrade"
    productPesIds="17081"
    supportTopicIds="32738517"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 
# I see a message that the Azure agent needs to be upgraded

## **Recommended Steps**

Do you see a message similar to the following when you open Azure Monitor for VMs?


![Azure Agent needs to be updated](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-azureagent/azure-agent-01.png?branch=pr-en-us-115799)

If so, we are unable to detect if the Azure Virtual Machine Agent (VM Agent) is running on your Azure VM.  In some cases, the Azure VM Agent is installed but is not working properly.  In this case, restarting the VM may correct the issue.

In other cases, the VM Agent version may be an earlier version that doesn't support the installation of our extensions or may not be installed at all.  In this case, please refer to these documents about getting the Azure VM Agent installed or updated on your Azure VM:  see this article for [Linux VMs](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-linux) and this article for [Windows VMs](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows).
