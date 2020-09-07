
<properties
    pageTitle="Linux Agent/Cannot uninstall agent"
    description="Cannot uninstall OMS Linux agent."
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    ms.author="johnkem"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612436"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="b14d2a39-2094-4a57-8645-7095056c5dd2"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/Cannot uninstall agent

## **Recommended Steps**

To resolve common uninstallation errors, try the following:

1. Review the [uninstall guide](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/OMS-Agent-for-Linux.md#uninstalling-the-oms-agent-for-linux) and verify that you are using one of the supported uninstall methods (dpkg, rpm, or the bundle .sh file with --remove)
2. Verify that the Linux Azure Diagnostic extension is not currently installed on the machine. The OMS Agent for Linux and Linux Azure Diagnostic extension share several components, so you must first uninstall the Linux Azure Diagnostic extension before uninstalling the OMS Agent for Linux. If you need to continue to use the Linux Azure Diagnostic extension, reinstall it after removing the OMS Linux Agent.
3. Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
4. Check the [agent log files](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#important-log-locations-and-log-collector-tool) and review the uninstall script output to identify any other errors

## **Recommended Documents**

* [Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
* [I'm unable to uninstall omsagent using purge option](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#im-unable-to-uninstall-omsagent-using-purge-option) <br>
* [Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)
