<properties
    pageTitle="Monitoring VMs: Performance Counters"
    description="Problems related to Performance Counters on Windows or Linux"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32633005"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="c56fa34c-f9e3-4a6b-ab81-af9193df342c"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Monitoring VMs: Performance Counter Issues on Windows or Linux

## **Recommended Steps**

To resolve common issues related to Performance Counters, try the following:

1. Ensure that the agent shows a health connection to the workspace. Run the below query in your workspace to see if the machine in question shows a recent heartbeat. If no heartbeat is found, please file a ticket under "Windows Agent" for "heartbeat data missing" and follow the recommended steps.

```
	Heartbeat
	| summarize arg_max(TimeGenerated, *) by Computer
```

2. Validate that you have [enabled the performance counter on your Log Analytics workspace](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-performance-counters#configuring-performance-counters):

	* In the Azure Portal, select your **Log Analytics workspaces** > your workspace > **Advanced Settings**. Select **Data**, and click **Windows** or **Linux Performance Counters**. Confirm that your log is listed. 
	
3. Restart the agent. Once the process restarts, wait approximately 5 minutes to see if the problem persists. 

	* If you are running a Linux machine: Restart the Log Analytics Agent by running `sudo /opt/microsoft/omsagent/bin/service_control restart`
	* If you are running a windows machine: Restart the Log Analytics Agent by running the following commands in an Administrative Command prompt: `net stop healthservice` followed by `net start healthservice`

4. Force a fresh configuration

	* For Linux machines, run `sudo -u omsagent python /opt/microsoft/omsconfig/Scripts/PerformRequiredConfigurationChecks.py`
	* For Windows machines, follow the below steps:
		1. Start an Administrative Command Prompt and run `Net Stop HealthService`
		2. Start File Explorer and navigate to `C:\Program Files` or `C:\Program Files(x86)`
		3. Go to this location: `Microsoft Monitoring Agent\Agent`
		4. Rename the folder **Health Service State** to **Old Health Service State**
		5. In the Administrative Command Prompt, run `Net Start Health Service`

4. Wait a few minutes, and [query your workspace](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-performance-counters#log-queries-with-performance-records) to check if event data is now being collected

## **Recommended Documents**

* [Windows and Linux Performance data sources in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-performance-counters)
