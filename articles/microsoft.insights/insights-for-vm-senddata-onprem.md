<properties
    pageTitle="I am having trouble sending data from my on-prem VMs to Azure"
    description="I am having trouble sending data from my on-prem VMs to Azure"
    infoBubbleText="Here are some things to help with getting your data to appear in Azure Monitor"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-senddata-onprem"
    productPesIds="17081"
    supportTopicIds="32738497"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 ## **Recommended Steps**

# I am having trouble sending data from my on-prem VMs to Azure

If you are unsure if the agents have installed properly, please refer to the support topic: I am having trouble installing the agents to my on-prem VM. 

### **VM doesn't appear in the Map view**

If installation of the Dependency agent succeeded, but you don't see your machine in the Map view: 

* Is the Dependency agent installed successfully? You can validate this by checking to see if the service is installed and running. 
  <br><br>**Windows**: Look for the service named Microsoft Dependency agent.  
  **Linux**: Look for the running process microsoft-dependency-agent.

* Are you on the [Log Analytics free tier](https://azure.microsoft.com/pricing/details/monitor/) (a Legacy pricing plan)? The Free plan allows for up to five unique Service Map machines. Any subsequent machines won't appear in Service Map, even if the prior five are no longer sending data. 
* Is your VM sending log and perf data to Azure Monitor Logs? Go to Azure Monitor\Logs and run the following query for your computer:  <br><br>`Usage | where Computer == "admdemo-appsvr" | summarize sum(Quantity), any(QuantityUnit) by DataType`<br><br>
Did you receive a variety of events in the results? Is the data recent? If so, your Log Analytics agent is operating correctly and communicating with the workspace. If not, check the agent on your machine: [Log Analytics agent for Windows troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows-troubleshoot) or [Log Analytics agent for Linux troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/agent-linux-troubleshoot). 

### **VM appears in Map but has no processes**

If you see your machine in the Map, but it has no process or connection data, that indicates that the Dependency agent is installed and running, but the kernel driver didn't load. 

Check the C:\Program Files\Microsoft Dependency Agent\logs\wrapper.log file (Windows) or /var/opt/microsoft/dependency-agent/log/service.log file (Linux). The last lines of the file should indicate why the kernel didn't load. For example, the kernel might not be supported on Linux if you updated your kernel. 


