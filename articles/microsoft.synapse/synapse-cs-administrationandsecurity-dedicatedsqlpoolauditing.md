<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783857"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Administration and Security/Dedicated SQL pool - Auditing"
    description = "Administration and Security/Dedicated SQL pool - Auditing"
    articleId = "synapse-cs-administrationandsecurity-dedicatedsqlpoolauditing.md"
    ms.author = "saltug,goventur"
/>

# Administration and Security/Dedicated SQL pool - Auditing

## **Recommended Steps**

* **Can [fn_get_audit_file()](https://docs.microsoft.com/sql/relational-databases/system-functions/sys-fn-get-audit-file-transact-sql?view=azure-sqldw-latest) be used to read audit files from Synapse dedicated SQL pool?**
  Yes, but the connection needs to be established to the logical server master database, or to an SQL DB database, and not to a Synapse database.

## **Recommended Documents** 

For getting started with auditing, refer to [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/) document.

For other security capabilities, refer to these documents:

* [SQL Pool Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)
* [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/)
* [Advanced data security](https://docs.microsoft.com/azure/sql-database/sql-database-advanced-data-security)

 