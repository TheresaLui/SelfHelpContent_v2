<properties
    pageTitle="Monitoring VMs: Windows Events"
    description="Problems related to Windows Events"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32633010"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="4b926241-7932-4f07-8f7b-1b2b46bda2ed"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Monitoring VMs: Windows Events Issues

## **Recommended Steps**

To resolve common issues related to Windows Events, try the following:

1. Ensure that the agent shows a health connection to the workspace. Run the below query in your workspace to see if the machine in question shows a recent heartbeat. If no heartbeat is found, please file a ticket under "Windows Agent" for "heartbeat data missing" and follow the recommended steps.

```
	Heartbeat
	| summarize arg_max(TimeGenerated, *) by Computer
```

2. Validate that you have [enabled the event on your Log Analytics workspace](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-windows-events#configuring-windows-event-logs):

	* In the Azure Portal, select your **Log Analytics workspaces** > your workspace > **Advanced Settings**. Select **Data**, and click **Windows Event Logs**. Confirm that your log is listed. 
	* Note that you need to [enable Security Center](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#data-collection-tier) if you want to collect “Windows Security Event"

3. Restart the Log Analytics Agent and Force a fresh configuration:

	1. Start an Administrative Command Prompt and run `Net Stop HealthService`
	2. Start File Explorer and navigate to `C:\Program Files` or `C:\Program Files(x86)`
	3. Go to this location: `Microsoft Monitoring Agent\Agent`
	4. Rename the folder **Health Service State** to **Old Health Service State**
	5. In the Administrative Command Prompt, run `Net Start Health Service`

4. Wait a few minutes, and [query your workspace](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-windows-events#log-queries-with-windows-events) to check if event data is now being collected

## **Recommended Documents**

* [Windows Event log data sources in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-windows-events)
