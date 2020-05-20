
<properties
    pageTitle="Linux Agent/Many instances of OMS agent running"
    description="Many instances of the OMS agent for Linux are running"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612486"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="951653da-b170-456a-8744-a2ebf5e610bb"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/Many instances of OMS agent running

## **Recommended steps**
If you see many instances of the omsagent process running, you can:

* Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Restart the machine.
* [Uninstall the current agent version](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/OMS-Agent-for-Linux.md#uninstalling-the-oms-agent-for-linux) then [install the latest version](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/OMS-Agent-for-Linux.md#steps-to-install-the-oms-agent-for-linux).

## **Recommended documents**

[Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
[Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)