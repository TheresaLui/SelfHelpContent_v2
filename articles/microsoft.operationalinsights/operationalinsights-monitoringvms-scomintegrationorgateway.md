
<properties
pageTitle="SCOM and Log Analytics integration issues"
description="SCOM and Log Analytics integration issues"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="deflection-SCOM_integration_or_LA_Gateway"
symptomID=""
infoBubbleText=""
authors="githitesh1"
ms.author="hishar"
displayorder=""
selfHelpType="generic"
supportTopicIds="32745399,32745400"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# SCOM and Log Analytics integration issues

Connecting Operations Manager with Azure Log Analytics allows you to collect machine data from your SCOM environment and analyze it in Azure Log Analytics. This self help document will cover the common integration issues between SCOM and Log analytics along with their recommended resolutions.


## **Recommended Steps**

* Unable to register SCOM to the log Analytics workspace? Connect Operations Manager to your Log Analytics workspace by [updating the SCOM management packs](https://azure.microsoft.com/updates/system-center-operations-manager-management-pack-to-configure-operations-management-suite/)
* Unable to connect Operations Manager to Log Analytics, status of SCOM says last data sent as "never": Re-configure Azure Log Analytics in SCOM
* Communication errors because of TLS version? Configure [MMA agent to use TLS 1.2](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#configure-agent-to-use-tls-12)
* Error Health Service event 8000: The Log Analytics workspace to which the MMA agent is connected is deleted and hence the MMA agent is causing this error <br>

## **Recommended Documents**

* [Connect SCOM to Azure Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/om-agents#connecting-operations-manager-to-azure-monitor)
* [Connect SCOM to a different Azure Log Analytics Workspace](https://docs.microsoft.com/azure/azure-monitor/platform/om-agents#switch-an-operations-manager-group-to-a-new-log-analytics-workspace)
* [Validate Operations Manager Integration with Azure Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/om-agents#validate-operations-manager-integration-with-azure-monitor)
* [Remove Operations Manager Integration with Azure Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/om-agents#remove-integration-with-azure-monitor)
