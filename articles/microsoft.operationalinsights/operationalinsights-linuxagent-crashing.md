
<properties
    pageTitle="Linux Agent/OMS agent: Crashing"
    description="OMS agent is crashing"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    ms.author="johnkem"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612497"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="dcc77a22-c4f2-4839-853a-c51a13462181"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/OMS agent: Crashing

## **Recommended Steps**

If you notice that the OMS agent for Linux is crashing frequently, try the following:

* Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Restart the OMS agent on the machine by running `sudo /opt/microsoft/omsagent/bin/service_control restart`
* Restart the machine

## **Recommended Documents**

* [Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
* [Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)
