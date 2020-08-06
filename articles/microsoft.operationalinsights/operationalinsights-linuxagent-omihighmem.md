
<properties
    pageTitle="Linux Agent/OMI process issues: Running high memory"
    description="OMI process has high memory consumption"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612496"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="430158ab-b890-473d-9eed-211da7503120"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/OMI process issues: Running high memory

## **Recommended steps**
If you notice that the OMI process is consuming a high amount of memory, try the following:

* Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Restart the OMI server daemon on the machine by running `sudo /opt/omi/bin/service_control restart`
* Restart the OMS agent on the machine by running `sudo /opt/microsoft/omsagent/bin/service_control restart`
* Restart the machine.

## **Recommended documents**

[Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
[Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)