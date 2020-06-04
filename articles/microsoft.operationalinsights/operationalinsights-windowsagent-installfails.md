
<properties
    pageTitle="Windows Agent: Installation fails"
    description="Cannot install Log Analytics Windows Agent"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612469"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="627dfbb1-a3f4-4f86-9562-4636370b9106"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Windows Agent: Installation fails

## **Recommended Steps**

To resolve common installation errors, try the following:

1. Verify that you are running a [supported version of the Windows OS](https://docs.microsoft.com/azure/azure-monitor/platform/log-analytics-agent#supported-windows-operating-systems)
2. If you had an issue with installing the agent via extension, and it now exists but is failing to connect, use one of the following methods to first uninstall the agent:

	* In the **Azure Portal**, select your workspace, click **Virtual machines**, and select the appropriate machine. Click **Disconnect**.
	* If the above fails, in the **Azure Portal**, click the **Virtual machines** blade and select your virtual machine. Then click on the **Extensions** blade. Uninstall the **MicrosoftMonitoringAgent**.
	* If both of the above fail, [use Powershell to Remove the agent extension](https://docs.microsoft.com/powershell/module/azurerm.compute/remove-azurermvmextension?view=azurermps-6.13.0)
	
3. Log into the machine with appropriate privileges to add and remove software. Click on the Windows start button and type "Add or Remove Programs". If the **Microsoft Monitoring Agent** is listed, click it, and choose **Uninstall**.
4. Open File Explorer and Navigate to `c:\Program Files` or `c:\Program Files(x86)`
5. Rename the folder “Microsoft Monitoring Agent” to “Old Microsoft Monitoring Agent”
6. Install the [Windows 64-bit agent](https://go.microsoft.com/fwlink/?LinkId=828603) or the [Windows 32-bit agent](https://go.microsoft.com/fwlink/?LinkId=828604) using your workspace id and key, and follow the steps given by the Installation Wizard. 
7. If you are trying to install the Log Analytics Extension on an Azure VM, try re-clicking **Connect**

## **Recommended Documents**

* [Installing the Windows Agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows) <br>
* [Powershell Installation of Windows Agent Extension](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-windows#powershell-deployment) <br>
