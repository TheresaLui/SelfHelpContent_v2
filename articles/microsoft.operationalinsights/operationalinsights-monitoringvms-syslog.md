<properties
    pageTitle="Monitoring VMs: Performance Counters"
    description="Problems related to Performance Counters on Windows or Linux"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="aliabuckner"
    ms.author="abuckner"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32633008"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="f007d6a8-45ed-46d5-a7bb-a543d07d7393"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Monitoring VMs: Syslog Problems related to Performance Counters on Windows or Linux

## **Recommended Steps**

To resolve common issues related to Performance Counters, try the following:

1. Ensure that the agent shows a health connection to the workspace. Run the below query in your workspace to see if the machine in question shows a recent heartbeat. If no heartbeat is found, please file a ticket under "Windows Agent" for "heartbeat data missing" and follow the recommended steps.

```
	Heartbeat
	| summarize arg_max(TimeGenerated, *) by Computer
```

2. Validate that you have [enabled the syslog facilities on your Log Analytics workspace](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-syslog#configuring-syslog)

	* In the Azure Portal, select your **Log Analytics workspaces** > your workspace > **Advanced Settings**. Select **Data**, and click **Syslog**. Confirm that your facility/facilities are listed. 

3. Restart the agent on the machine by running `sudo /opt/microsoft/omsagent/bin/service_control restart`. Once the process restarts, wait approximately 5 minutes to see if the problem persists. If you are running a Windows machine: Restart the Log Analytics Agent by running the following commands in an Administrative Command prompt: `net stop healthservice` followed by `net start healthservice`.
	
4. To force a fresh configuration for the agent run `sudo -u omsagent python /opt/microsoft/omsconfig/Scripts/PerformRequiredConfigurationChecks.py`
5. Wait a few minutes, and [query your workspace](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-syslog#log-queries-with-syslog-records) to check if Syslog data is now being collected

## **Recommended Documents**

* [Syslog data sources in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-syslog)
