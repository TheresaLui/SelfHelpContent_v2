
<properties
    pageTitle="Linux Agent/OMS agent: Running high CPU"
    description="OMS agent has high CPU utilization"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612498"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="457760c5-85c3-44c2-bc90-4ecf5a471775"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/OMS agent: Running high CPU

## **Recommended steps**
If you notice that the OMS agent process is consuming a high amount of CPU resources, try the following:

* Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Restart the OMS agent on the machine by running `sudo /opt/microsoft/omsagent/bin/service_control restart`
* Restart the machine.

## **Recommended documents**

[Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
[Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)