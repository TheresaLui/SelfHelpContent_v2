 
<properties
pageTitle="Move SQL Resources Between Subscriptions"
description="Move SQL Resources Between Subscriptions"
ms.author="keithelm"
displayOrder=""
articleId="ccfc29ea-d4ce-4a4b-9f87-57d0d5f31b19"
selfHelpType="Apollo"
supportTopicIds=""
productPesIds="13491"
cloudEnvironments="public"
mappedToBucket="true"
ownershipId="AzureData_AzureSQLDB"
/>

# Move SQL Resources Between Subscriptions
 

## Move SQL resources between subscriptions

Azure SQL Database supports resource migration (server, database, elastic pool, etc) between resource groups or subscriptions. When you move a SQL server, all of its databases are also moved.

Migration between resource groups and subscriptions is a metadata-only operation. Connections to the server and database are not impacted; all data and settings are preserved. The resource group is locked from other changes during the operation. 

## Resources
See [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription) for more detailed instructions, restrictions and frequently asked questions.

See [Move operation support for resources](https://docs.microsoft.com/azure/azure-resource-manager/management/move-support-resources) to check the support status of moving other non-SQL Database resources.

