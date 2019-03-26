
<properties
    pageTitle="Windows Agent: Cannot Uninstall Agent"
    description="Cannot uninstall Log Analytics Windows Agent"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612437"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax"
	articleId="dcc77a22-c4f2-4839-853a-c51a13462181"
/>

# Windows Agent: Cannot uninstall agent

## **Recommended steps**
To resolve common uninstallation errors, try the following:

* Restart the Log Analytics Agent by running the following commands in an Administrative Command prompt: 'net stop healthservice' followed by 'net start healthservice'. Once the process restarts, wait approximately 5 minutes to see if the problem persists. 
* If you are running an Azure VM with the Log Analytics VM Extension, try the following:
	* In the **Azure Portal**, select your workspace, click **Virtual machines**, and select the appropriate machine. Click **Disconnect**.
	* If the above fails, in the **Azure Portal**, click the **Virtual machines** blade and select your virtual machine. Then click on the **Extensions** blade. Uninstall the **MicrosoftMonitoringAgent**
	* If both of the above fail, [use Powershell to Remove the Log Analytics Agent Extension](https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension?view=azurermps-6.13.0)
* Uninstall Windows Log Analytics Agent via Control Panel
	1. Log onto the machine with appropriate priveleges to add and remove software
	2. Click on the Windows start button and type "Add Remove Programs"
	3. Locate **Microsoft Monitoring Agent**, click it, and choose **Uninstall**


## **Recommended documents**

[How to Clear the Agent Cache](https://docs.microsoft.com/en-us/system-center/scom/manage-clear-healthservice-cache?view=sc-om-2019#to-clear-the-cache) <br>
[Uninstall Windows Log Analytics Agent via Control Panel](https://docs.microsoft.com/en-us/azure/azure-monitor/learn/quick-collect-windows-computer#clean-up-resources) <br>
[Powershell Removal of Windows Log Analytics Agent Extension](https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension?view=azurermps-6.13.0)