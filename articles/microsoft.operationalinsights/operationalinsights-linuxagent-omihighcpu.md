<properties
  pagetitle="Linux Agent/OMI process issues: Running high CPU&#xD;"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="luki"
  selfhelptype="Generic"
  supporttopicids="32612495"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,blackforest,fairfax,usnat,ussec,mooncake"
  disableclouds=""
  articleid="a353d6c5-ffe0-4632-a750-f79718c8a9f9"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Linux Agent/OMI process issues: Running high CPU

## **Recommended Steps**

If you notice that the OMI process is consuming a high amount of CPU resources, try the following:

* Make sure that you are running the [latest version of the agent](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#agent-and-vm-extension-version). You can see if you have the latest version by running `sudo sh ./omsagent-*.universal.x64.sh --version-check` on the machine. If you are not running the latest version, you can run `sudo sh ./omsagent-*.universal.x64.sh --upgrade` to upgrade.
* Restart the OMI server daemon on the machine by running `sudo /opt/omi/bin/service_control restart`
* Restart the OMS agent on the machine by running `sudo /opt/microsoft/omsagent/bin/service_control restart`
* Restart the machine.

## **Recommended Documents**

[Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
[Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)
