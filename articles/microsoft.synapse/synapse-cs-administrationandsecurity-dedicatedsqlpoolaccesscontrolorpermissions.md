<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783856"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Administration and Security/Dedicated SQL pool - Access control or permissions"
    description = "Administration and Security/Dedicated SQL pool - Access control or permissions"
    articleId = "synapse-cs-administrationandsecurity-dedicatedsqlpoolaccesscontrolorpermissions.md"
    ms.author = "saltug"
/>

# Administration and Security/Dedicated SQL pool - Access control or permissions

## **Recommended Steps**

The following details explain how to set up and update common access and permissions rules in Dedicated SQL pool. 

* If you're looking to change the administrator password for a Dedicated SQL pool in Synapse Workspace, you can simply click "Reset SQL admin password" at the top of the Synapse workspace resource blade

* If you're looking to change the administrator password for a Synapse Dedicated SQL pool (data warehouse), you can simply click "Reset Password" at the top of the SQL Server resource blade

* Follow the configuration steps to set-up and connect to Dedicated SQL pool using [Azure Active Directory](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-authentication/) authentication

* [Secure a Dedicated SQL pool](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)

### What access control can be done at the server level

* Server-level permissions are not available in Synapse SQL. For more information, see [Using fixed and custom database roles](https://docs.microsoft.com/azure/sql-database/sql-database-manage-logins#using-fixed-and-custom-database-roles).

## **Recommended Documents**

* [SQL Pool Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)
* [SQL Pool Access Control Overview](https://docs.microsoft.com/azure/sql-database/sql-database-manage-logins?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json)
* [Database-Level Roles](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/database-level-roles?view=sql-server-ver15)
* [SQL Permissions](https://docs.microsoft.com/sql/relational-databases/security/permissions-database-engine?view=sql-server-ver15)
* [SQL Security Overview](https://docs.microsoft.com/azure/sql-database/sql-database-security-overview)

 