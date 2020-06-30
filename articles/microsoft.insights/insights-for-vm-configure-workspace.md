<properties
  pageTitle="I can't configure my Log Analytics workspace"
    description="I can't configure my Log Analytics workspace"
    infoBubbleText="Here are some things to help with workspace setup"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-configure-workspace"
    productPesIds="17081"
    supportTopicIds="32738505"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />


# I can't configure my Log Analytics workspace #

## **Recommended Steps**

For the views in Azure Monitor for VMs to display the data correctly, you need to have your Log Analytics workspace configured with our monitoring solution.  In addition, the workspace needs to be in a supported region.VMs from any location can be monitored with Azure Monitor for VMs as long as they send data to a workspace in a supported region. 

### **Is your workspace in a supported region?**

[Refer to our documentation](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-overview#log-analytics) to verify your workspace is in a supported region. 

If you don't have a workspace, you can create one using one of the following methods [described in our documentation](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-overview#log-analytics). 

### **Do you have the correct permissions to install the solution in the workspace?**

You need to be a member of the Log Analytics contributor role to install the solution.  Please [refer to our documentation](https://docs.microsoft.com/azure/azure-monitor/platform/manage-access#manage-access-using-workspace-permissions) for the specific Azure permissions needed. 

### **Is the solution installed in the workspace?**

Navigate to the Log Analytics workspace, choose Solutions from the left-hand pane, and verify you see **VMInsights** listed an installed solution. 

![Workspace solutions](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-workspacesetup/solutions-01.png?branch=pr-en-us-115799)

If the solution is not installed, you can use the workspace configuration tool from the Get Started page to easily install it.  You can access this page from Monitor\Insights - Virtual Machines\Get Started.  Select the tab for **Other onboarding options** and select the **Configure** option in the link in the **Configure a workspace** tile. Choose the target workspace and it installs the solution for you. 

![Setup Workspace](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-workspacesetup/configure-01.png?branch=pr-en-us-115799) 

If you want to learn how to script workspace setup, [refer to this documentation](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-enable-at-scale-powershell#set-up-a-log-analytics-workspace). 

