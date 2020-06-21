
<properties
    pageTitle="Windows Agent: Running high memory or CPU"
    description="Windows agent is consuming high amount of memory of CPU resources"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612489"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="679eb12d-b48f-4ccd-b3ff-fe75d244bf75"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Windows Agent: Running high memory or CPU

## **Recommended Steps**

**Note**: Adding certain solutions to your workspace will result in increased workload for the agent. It is normal for the agent to continue to run high memory and/or CPU for up to 30 minutes following such events. 

If you notice that the Log Analytics agent for Windows is consuming a high amount of memory or CPU resources, try the following: 

* Restart the Log Analytics Agent by running the following commands in an Administrative Command prompt: `net stop healthservice` followed by `net start healthservice`. Once the process restarts, wait approximately 5 minutes to see if the problem persists. 

* [Clear the agent cache](https://docs.microsoft.com/system-center/scom/manage-clear-healthservice-cache?view=sc-om-2019#to-clear-the-cache):

	1. In the **Monitoring** workspace, expand **Operations Manager** and then expand **Agent Details**
	2. Click **Agent Health State**
	3. In **Agent State**, select an agent
	4. In the **Tasks** pane, click **Flush Health Service State and Cache**
	5. Wait a few minutes, and try querying again for your desired data

* Force a fresh configuration:

	1. Start an Administrative Command Prompt and run 'Net Stop HealthService'
	2. Start File Explorer and navigate to `C:\Program Files` or `C:\Program Files(x86)`
	3. Go to this location: `Microsoft Monitoring Agent\Agent`
	4. Rename the folder **Health Service State** to **Old Health Service State**
	5. In the Administrative Command Prompt, run `Net Start Health Service`

* [Verify agent connectivity to Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#verify-agent-connectivity-to-log-analytics):

	* From the computer in **Control Panel**, find the item **Microsoft Monitoring Agent**. Select it and on the **Azure Log Analytics** tab, the agent should display a message stating: "The Microsoft Monitoring Agent has successfully connected to the Microsoft Operations Management Suite Service."

* If the agent has not successfully connected to Log Analytics, ensure that you have [properly configured your proxy settings](https://docs.microsoft.com/azure/azure-monitor/platform/agent-manage#windows-agent-1):

	1. Sign on the computer with an account that has administrative rights
	2. Open **Control Panel**
	3. Select **Microsoft Monitoring Agent** and then click the **Proxy Settings** tab
	4. Click **Use a proxy server** and provide the URL and port number of the proxy server or gateway. If your proxy server or Log Analytics gateway requires authentication, type the username and password to authenticate and then click **OK**. 

* If you do not have the latest version of the agent:

	* If you are running an Azure VM with the Log Analytics VM Extension: in the **Azure Portal**, select your workspace, click **Virtual machines**, and select the machine which is crashing. Click **Disconnect**. When the disconnect is complete, click **Connect** to reinstall the latest agent/extension. 
	* If you are not using an extension or you are using an on-prem machine: [Uninstall the current agent version](https://docs.microsoft.com/azure/azure-monitor/platform/agent-manage#uninstall-agent), then [install the latest Log Analytics Agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard) directly on the VM

## **Recommended Documents**

* [Installing the Windows Agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows) <br>
* [Troubleshooting the Windows VM Extension](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot#troubleshooting-azure-windows-vm-extension) <br>
* [Powershell Installation of Windows Agent Extension](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-windows#powershell-deployment) <br>
* [Powershell Removal of Windows Agent Extension](https://docs.microsoft.com/powershell/module/azurerm.compute/remove-azurermvmextension?view=azurermps-6.13.0)
