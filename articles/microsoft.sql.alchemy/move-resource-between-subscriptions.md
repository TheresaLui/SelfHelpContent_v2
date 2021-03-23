 
<properties
pageTitle="Move SQL Resources Between Subscriptions"
description="Move SQL Resources Between Subscriptions"
ms.author="keithelm"
displayOrder=""
articleId="ccfc29ea-d4ce-4a4b-9f87-57d0d5f31b19"
selfHelpType="Apollo"
supportTopicIds="32780633	"
productPesIds="13491"
cloudEnvironments="public"
mappedToBucket="false"
ownershipId="AzureData_AzureSQLDB"
/>

# Move SQL Resources Between Subscriptions
 

## Move SQL Resources Between Subscriptions

SQL Database supports [resource migration](https://docs.microsoft.com/azure/azure-resource-manager/management/move-support-resources#microsoftsql) (server, database, elastic pool, etc) between resource groups or subscriptions. When you move a SQL server, all its databases are also moved.

Migration between resource groups/subscriptions is a metadata operation. The resource group is locked from other changes during the operation, but connections to the server/database are not impacted.  All data is preserved during the operation.  See [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) for more detailed instructions and frequently asked questions.

