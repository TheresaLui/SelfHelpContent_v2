<properties
    pageTitle="The performance view is blank or shows partial data"
    description="The performance view is blank or shows partial data"
    infoBubbleText="Here are some things to help with the performance view"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-agent-performance-view-blank"
    productPesIds="17081"
    supportTopicIds="32738521"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 # The performance view is blank or shows partial data

 ## **Recommended Steps**

If you are unsure if the extensions or agents have installed properly, please refer to the support topics: *I cannot get the VM extensions to install on my Azure VM* and *I am having trouble installing the agents to my on-prem VM*.

### **There is no data on the performance charts for my VM**

If installation of the log analytics agent succeeded, but you don't see data on the Performance view take a look at the following.

**Is your VM sending log and perf data to Azure Monitor Logs?**

*  Go to Azure Monitor\Logs and run the following query for your computer: 
* `Usage | where Computer == "admdemo-appsvr" | summarize sum(Quantity), any(QuantityUnit) by DataType`
* Did you receive a variety of events in the results? Is the data recent? If so, your Log Analytics agent is operating correctly and communicating with the workspace. If not, check the agent on your machine: [Log Analytics agent for Windows troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows-troubleshoot) or [Log Analytics agent for Linux troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/agent-linux-troubleshoot). 

**Is you workspace setup to collect the performance counters?**

As part of enabling Azure Monitor for VMs we setup several performance counters on your workspace.  

**Setup the workspace performance counters**

You can use the workspace configuration tool from the Get Started page to easily setup the performance counters.  You can access this page from Monitor\Insights - Virtual Machines\Get Started.  Select the tab for **Other onboarding options** and select the **Configure** option in the link in the **Configure a workspace** tile. Choose the target workspace and it installs the solution for you. 

![Setup Workspace](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-workspacesetup/configure-01.png?branch=pr-en-us-115799) 
