<properties
    pageTitle="ARM Activity Log"
    description="Get activity log for all Azure Cosmos DB Azure Resource Manager (ARM) requests"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32681007"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-admin-arm-activity-log"
    displayOrder="27"
    category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Resource Manager (ARM) Deployments
Most users are able to resolve their Azure Resource Manager (ARM) Deployments issue using the steps below.

## **Recommended Steps**

Azure provides an [activity log](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-audit) that contains all write operations (PUT, POST, DELETE) for your resources. It doesn't include read operations (GET). You can use the activity logs to find an error when troubleshooting or to monitor how a user in your organization modified a resource. Through activity logs, you can determine:

- What operations were taken on the resources in your subscription
- Who started the operation
- When the operation occurred
- The status of the operation
- The values of other properties that might help you research the operation

Activity logs are kept for 90 days. You can query for any range of dates, as long as the starting date isn't more than 90 days in the past.


### **Error Message: Provided list of regions contains duplicate regions. Please remove duplicates...**  
ARM template will read the same Resource Group location twice and place it into different locations causing *Provided list of regions contains duplicate regions. Please remove duplicates...* 
 
You need to choose one of the following alternatives:
- Remove the location with failoverPriority: 1 (to have only one region)
- Change template so second entry properties has a different locationName



## **Recommended Documents**

[Azure Activity Logs](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-audit)
<br>Through activity logs, you can determine:  
- What operations were taken on the resources in your subscription
- Who started the operation
- When the operation occurred
- The status of the operation
- The values of other properties that might help you research the operation  

[Azure Resource Manager Resource Provider operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
<br>This article lists the operations available for each Azure Resource Manager resource provider. These operations can be used in custom roles to provide granular role-based access control (RBAC) to resources in Azure.
