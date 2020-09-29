
<properties
pageTitle="Workspace ARM template deployment issues"
description="Workspace ARM template deployment issues"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="b9bad328-2ce5-449a-a4d7-6d86c5421fc6"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612544"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Workspace ARM template deployment issues
Workspace deployment at scale can be made easier with ARM template using PowerShell or CLI.

## **Recommended Steps**

* Follow this sample to [create a workspace ARM template](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace-posh#create-and-deploy-template)
* Deploy template using [Azure CLI](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace-cli)
* Deploy template using [PowerShell](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace-posh)
* [Configure your template](https://docs.microsoft.com/azure/azure-monitor/platform/template-workspace-configuration#configure-a-log-analytics-workspace) to add solutions, create saved searches and collect data sources.<br>

If you are getting an error when updating a SavedSearch, add 'etag' in the body of the API or the Azure Resource Manager template properties:

```
"properties": {
"etag": "*",
   "query": "SecurityEvent | where TimeGenerated > ago(1h) | where EventID == 4625 | count",
   "displayName": "An account failed to log on",
   "category": "Security"
}
```

## **Recommended Documents**

* Follow this sample to [create a workspace template](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace-posh#create-and-deploy-template)
* Deploy template using [Azure CLI](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace-cli)
* Deploy template using [PowerShell](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace-posh)
* [Configure your template](https://docs.microsoft.com/azure/azure-monitor/platform/template-workspace-configuration#configure-a-log-analytics-workspace)
* [Azure Monitor PowerShell quick start samples](https://docs.microsoft.com/azure/azure-monitor/platform/powershell-quickstart-samples)
* [Understand the structure and syntax of Azure Resource Manager Templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-authoring-templates)<br>
