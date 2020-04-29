
<properties
    pageTitle="Linux Agent/OMS agent: Running high memory"
    description="OMS agent has high memory consumption"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612499"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="c3ef72a1-f525-4fa8-8ae7-4b11d662de4d"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/OMS agent: Running high memory

## **Recommended steps**
If you notice that the OMS agent for Linux is consuming a high amount of memory, try the following:

* Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Restart the OMS agent on the machine by running `sudo /opt/microsoft/omsagent/bin/service_control restart`
* Restart the machine.

## **Recommended documents**

[Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
[Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)