<properties
    pageTitle="Cannot open server y requested by the login"
    description="Cannot open server y requested by the login"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745431"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="C276D6F0-89C7-4689-B870-4D838304F292"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Cannot open server y requested by the login

## **Recommended Steps**

### Error 40615: Cannot open server y requested by the login

* To be able to create and manage IP firewall rules for the Azure SQL Server, you will need to either be:

 * In the [SQL Server Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles?WT.mc_id=pid:13491:sid:32745431/#sql-server-contributor) role
 * In the [SQL Security Manager](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles?WT.mc_id=pid:13491:sid:32745431/#sql-security-manager) role
 * The owner of the resource that contains the Azure SQL Server

There are two types of firewall rules:

* **Server level firewall rules**: These rules enable clients to access your entire server, that is, all the databases managed by the server. The rules are stored in the master database. You can have a maximum of 128 server-level IP firewall rules for a server. If you have the Allow Azure Services and resources to access this server setting enabled, this counts as a single firewall rule for the server. These can be managed using various ways mentioned below. If you are facing issues using one way please try an alternate approach.

  * [Azure Portal](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid:13491:sid:32745431/#create-and-manage-ip-firewall-rules)
  * [PowerShell](https://docs.microsoft.com/powershell/module/az.sql/?WT.mc_id=pid:13491:sid:32745431&view=azps-4.5.0&viewFallbackFrom=azps-4.2.0)
  * [Azure CLI](https://docs.microsoft.com/cli/azure/sql/server/firewall-rule?WT.mc_id=pid:13491:sid:32745431&view=azure-cli-latest)
  * [T-SQL](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid:13491:sid:32745431/#create-and-manage-ip-firewall-rules)
  * [Rest-API](https://docs.microsoft.com/rest/api/sql/firewallrules/createorupdate?WT.mc_id=pid:13491:sid:32745431)

To improve performance, server-level IP firewall rules are temporarily cached at the database level. To refresh the cache, see [DBCC FLUSHAUTHCACHE](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-flushauthcache-transact-sql?WT.mc_id=pid:13491:sid:32745431&redirectedfrom=MSDN&view=azuresqldb-current).

* **Database level firewall rules**: These rules enable clients to access certain (secure) databases. You create the rules for each database (including the master database), and they're stored in the individual database. It is recommended to use database-level IP firewall rules whenever possible. This practice enhances security and makes your database more portable. These can be managed only using T-SQL.

* [sys.database_firewall_rules](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-database-firewall-rules-azure-sql-database?WT.mc_id=pid:13491:sid:32745431&view=azuresqldb-current)
* [sp_set_database_firewall_rule](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-set-database-firewall-rule-azure-sql-database?WT.mc_id=pid:13491:sid:32745431&view=azuresqldb-current)
* [sp_delete_database_firewall_rule](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-delete-database-firewall-rule-azure-sql-database?WT.mc_id=pid:13491:sid:32745431&view=azuresqldb-current)

### Troubleshooting the database firewall

If you are seeing that the firewall rules are not behaving as expected, please follow the [recommendations](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid:13491:sid:32745431#troubleshoot-the-database-firewall).

## **Recommended Documents**

 * [Create and manage firewall rules](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid:13491:sid:32745431)
 * [Virtual network endpoints](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview?WT.mc_id=pid:13491:sid:32745431)
 * [PowerShell create virtual service endpoint](https://docs.microsoft.com/azure/azure-sql/database/scripts/vnet-service-endpoint-rule-powershell-create?WT.mc_id=pid:13491:sid:32745431)
