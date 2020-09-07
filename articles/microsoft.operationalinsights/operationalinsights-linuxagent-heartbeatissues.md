
<properties
    pageTitle="Linux Agent/HeartBeat-related issues"
    description="Issues with the Heartbeat solution for the OMS Linux Agent."
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    ms.author="johnkem"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612462"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, BlackForest, Fairfax, MoonCake, usnat, ussec"
	articleId="54b81f5f-a9f3-48a6-87cb-bbb92ee1ddae"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/HeartBeat-related issues

## **Recommended Steps**

If you are not seeing any heartbeat data in Log Analytics, try the following:

* Ensure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Ensure that you have [properly configured your proxy settings](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#im-unable-to-connect-through-my-proxy-to-oms)
* Restart the OMI server daemon on the machine by running `sudo /opt/omi/bin/service_control restart`
* Restart the machine
* Ensure that the agent successfully onboarded to the OMS Service by verifying that this file exists: `/etc/opt/microsoft/omsagent/<workspace id>/conf/omsadmin.conf`. The file will only exist if the agent successfully onboarded. If the file does not exist, review the [common onboarding error codes](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#onboarding-error-codes) and attempt to re-onboard the agent:<br>

```
cd /opt/microsoft/omsagent/bin
sudo ./omsadmin.sh -w <WorkspaceID> -s <WorkspaceKey>
```

## **Recommended Documents**

* [Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
* [I'm not seeing any Linux data in the OMS Portal](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#im-not-seeing-any-linux-data-in-the-oms-portal) <br>
* [Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)
