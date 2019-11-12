<properties
    pageTitle="ARM Activity Log"
    description="Get activity log for all Azure Cosmos DB Azure Resource Manager (ARM) requests"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="markjbrown"
    ms.author="mjbrown"
    selfHelpType="resource"
    supportTopicIds="32681007"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
    articleId="cosmosdb-admin-arm-activity-log"
    displayOrder="27"
    category="Administration"
/>

# Troubleshooting Azure Resource Manager (ARM) Deployments

Azure provides an [activity log](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-audit) that contains all write operations (PUT, POST, DELETE) for your resources. It doesn't include read operations (GET). You can use the activity logs to find an error when troubleshooting or to monitor how a user in your organization modified a resource. Through activity logs, you can determine:

- What operations were taken on the resources in your subscription
- Who started the operation
- When the operation occurred
- The status of the operation
- The values of other properties that might help you research the operation

* For information on how to use Azure Activity log see, [View activity logs to monitor actions on resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-audit)
* For a list of resource actions for Azure Cosmos DB see, [Azure Resource Manager Resource Provider operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)

Activity logs are kept for 90 days. You can query for any range of dates, as long as the starting date isn't more than 90 days in the past.

## **Recommended Documents**

- [Azure Activity Logs](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-audit)
- [Azure Resource Manager Resource Provider operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
- [Azure Cosmos DB Resource Provider Operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
