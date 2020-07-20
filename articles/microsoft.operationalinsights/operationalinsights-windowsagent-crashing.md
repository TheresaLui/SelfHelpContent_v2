
<properties
    pageTitle="Windows Agent: Crashing"
    description="Windows agent is crashing"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612488"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="fb11928a-1782-4618-a046-eb29996ee084"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Windows Agent: Crashing

## **Recommended Steps**

If you notice that the OMS agent for Windows is crashing frequently, try the following:

* Restart the Log Analytics Agent by running the following commands in an Administrative Command prompt: `net stop healthservice` followed by `net start healthservice`. Once the process restarts, wait approximately 5 minutes to see if the problem persists. 
* If you are running an Azure VM with the Log Analytics VM Extension: in the **Azure Portal**, select your workspace, click **Virtual machines**, and select the machine which is crashing. Click **Disconnect**. When the disconnect is complete, click **Connect** to reinstall the latest agent/extension. 
* If you are not using an extension or you are using an on-prem machine: [Uninstall the current agent version](https://docs.microsoft.com/azure/azure-monitor/platform/agent-manage#uninstall-agent), then [install the latest Log Analytics Agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard) directly on the VM

## **Recommended Documents**

* [Installing the Windows Agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows) <br>
* [Troubleshooting the Windows VM Extension](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot#troubleshooting-azure-windows-vm-extension) <br>
* [Powershell Installation of Windows Agent Extension](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-windows#powershell-deployment) <br>
* [Powershell Removal of Windows Agent Extension](https://docs.microsoft.com/powershell/module/azurerm.compute/remove-azurermvmextension?view=azurermps-6.13.0)
