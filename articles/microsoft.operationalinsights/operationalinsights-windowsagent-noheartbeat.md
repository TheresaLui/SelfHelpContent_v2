
<properties
    pageTitle="Windows Agent: Not reporting data or Heartbeat data missing"
    description="Windows agent is not reporting heartbeat or other data"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32745396"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="ef27edc9-33f4-4e95-9a69-a22050c84cf7"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Windows Agent: Not reporting data or Heartbeat data missing

## **Recommended Steps**

Verify that you are running a [supported version of the Windows OS](https://docs.microsoft.com/azure/azure-monitor/platform/log-analytics-agent#supported-windows-operating-systems). 

### The agent has ***never*** sent any data, or has stopped sending ***all*** data

* [Verify agent connectivity to Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#verify-agent-connectivity-to-log-analytics):

	* From the computer in **Control Panel**, find the item **Microsoft Monitoring Agent**. Select it and on the **Azure Log Analytics** tab, the agent should display a message stating: "The Microsoft Monitoring Agent has successfully connected to the Microsoft Operations Management Suite Service." 

* If the agent has not successfully connected to Log Analytics, ensure that you have [properly configured your proxy settings](https://docs.microsoft.com/azure/azure-monitor/platform/agent-manage#windows-agent-1):

	1. Sign on the computer with an account that has administrative rights
	2. Open **Control Panel**
	3. Select **Microsoft Monitoring Agent** and then click the **Proxy Settings** tab
	4. Click **Use a proxy server** and provide the URL and port number of the proxy server or gateway. If your proxy server or Log Analytics gateway requires authentication, type the username and password to authenticate and then click **OK**.
	
* Restart the Log Analytics Agent by running the following commands in an Administrative Command prompt: `net stop healthservice` followed by `net start healthservice`. Once the process restarts, wait approximately 5 minutes to see if the problem persists. 

### The agent is reporting ***some*** data, but not all

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

## **Recommended Documents**

* [Installing the Windows Agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows) <br>
* [Troubleshooting the Windows VM Extension](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot#troubleshooting-azure-windows-vm-extension) <br>
