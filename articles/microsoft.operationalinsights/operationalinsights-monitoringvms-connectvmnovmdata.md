
<properties
pageTitle="Connect VM to workspace or no VM data in workspace"
description="Connect VM to workspace or no VM data in workspace"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="4c3ff6c4-414f-4c2d-89f7-26f3bbbfa2db"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32745397,32745398"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Connect VM to workspace or no VM data in workspace

## **Recommended Steps**
* If you fail to disconnect Linux agent from the VM, try using the latest [OMS Agent for Linux](https://github.com/Microsoft/OMS-Agent-for-Linux) package with --purge.
* If you want to receive logs from a VM that doesn't have connection to the Internet, try to [Connect computers without Internet access using the Log Analytics gateway](https://docs.microsoft.com/azure/azure-monitor/platform/gateway)<br>

## **Recommended Documents**
* [Troubleshooting the Log Analytics VM extension](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot)
* [How to troubleshoot issues with the Log Analytics agent for Linux](https://docs.microsoft.com/azure/azure-monitor/platform/agent-linux-troubleshoot)
* [Log Analytics virtual machine extension for Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux)
* [Log Analytics virtual machine extension for Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-windows)
* [Linux agent installation Error Codes](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#installation-error-codes)
* [Linux agent troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/platform/agent-linux-troubleshoot)
* [Connect Windows computers to Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)
* [Managing and maintaining the Log Analytics agent for Windows and Linux](https://docs.microsoft.com/azure/azure-monitor/platform/agent-manage)<br>