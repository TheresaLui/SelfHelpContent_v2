
<properties
pageTitle="Permissions and access control (IAM)"
description="Permissions and access control (IAM)"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="meirm"
ms.author="meirm"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612439"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
articleId="bd047e2f-6aa4-4218-a8a8-059135dbc5f2"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Permissions and access control (IAM)

## **Recommended Steps** 

### **Are you using resource-context or workspace-context?**
When executing a query, you may use the context of an Azure resource or resource-group or subscription. In that case:
1.	You should have read access to the resource
2.	The workspace shall have [access control mode](https://docs.microsoft.com/azure/azure-monitor/platform/design-logs-deployment#access-control-mode) set to “Use resource or workspace permissions:”
When executing a query in the context of a workspace, only the workspace permissions are evaluated. 

### **Check workspace and resource permissions using the Azure portal**
You can check workspace or resource access rights of a user as explained [here](https://docs.microsoft.com/azure/role-based-access-control/check-access).

## **Recommended Documents**

* [Manage access to log data and workspaces in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/manage-access)
* [Designing your Azure Monitor Logs deployment](https://docs.microsoft.com/azure/azure-monitor/platform/design-logs-deployment)
