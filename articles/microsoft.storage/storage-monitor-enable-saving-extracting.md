<properties
	pageTitle="Issues with enabling, saving, extracting diagnostics logs"
	description="Issues with enabling, saving, extracting diagnostics logs"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="Rashmian"
	ms.author="Rashmia"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32681421,32681659,32681660,32681661,32681662"
	resourceTags=""
	productPesIds="15629, 16459, 16460, 16462, 16461, 16598"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="13bfde3a-0849-44fc-bf30-b736e7d20d4c"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Issues with enabling, saving, extracting diagnostics logs

## **Recommended Documents**

* [Create diagnostic settings in Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-diagnostic-settings-in-azure-portal)<br>
* [Create diagnostic settings using PowerShell](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-diagnostic-settings-using-powershell)<br>
* [Create diagnostic settings using Azure CLI](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-diagnostic-settings-using-azure-cli)<br>
* [Consuming diagnostics logs from a Log Analytics workspace](https://docs.microsoft.com/azure/cdn/cdn-azure-diagnostic-logs#consuming-diagnostics-logs-from-a-log-analytics-workspace)<br>

### **Note** 

Azure Data Lake Storage Gen2 accounts are not currently supported as a destination for diagnostic settings even though they may be listed as a valid option in the Azure portal.

Following documents has additional information related to this issue: 

*  Refer to [prerequisites](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs-collect-storage#prerequisites) document for more information
* Refer to  [destinations](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#destinations) for sending data to different destinations
