<properties
	pageTitle="create drop and manage resources/firewall rules"
	description="create drop and manage resources/firewall rules"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa,andikshi"
    ms.author="emlisa,andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630421, 32745431"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="66d117ce-0066-4e22-96a9-5a931234316c-new-st"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# create drop and manage resources/firewall rules

## **Recommended Steps**

To be able to create and manage IP firewall rules for the Azure SQL Server, you will need to either be:

* In the [SQL Server Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-server-contributor) role
* In the [SQL Security Manager](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-security-manager) role
* The owner of the resource that contains the Azure SQL Server

There are two types of firewall rules :

1. Server level firewall rules:

These rules enable clients to access your entire server, that is, all the databases managed by the server. The rules are stored in the master database. You can have a maximum of 128 server-level IP firewall rules for a server. If you have the Allow Azure Services and resources to access this server setting enabled, this counts as a single firewall rule for the server. These can be managed using various ways mentioned below. If you are facing issues using one way please try an alternate approach.

* [Azure Portal](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid%3A13491%3Asid%3A32630421%2F#create-and-manage-ip-firewall-rules)
* [PowerShell](https://docs.microsoft.com/powershell/module/az.sql/?view=azps-4.2.0)
* [Azure CLI](https://docs.microsoft.com/cli/azure/sql/server/firewall-rule?view=azure-cli-latest)
* [T-SQL](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid%3A13491%3Asid%3A32630421%2F#create-and-manage-ip-firewall-rules)
* [Rest-API](https://docs.microsoft.com/rest/api/sql/firewallrules/createorupdate)

To improve performance, server-level IP firewall rules are temporarily cached at the database level. To refresh the cache, see [DBCC FLUSHAUTHCACHE](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-flushauthcache-transact-sql?redirectedfrom=MSDN&view=azuresqldb-current).

2. Database level firewall rules:

These rules enable clients to access certain (secure) databases. You create the rules for each database (including the master database), and they're stored in the individual database.It is recommended to use database-level IP firewall rules whenever possible. This practice enhances security and makes your database more portable.
These can be managed only using T-SQL.

* [sys.database_firewall_rules](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-database-firewall-rules-azure-sql-database)
* [sp_set_database_firewall_rule](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-set-database-firewall-rule-azure-sql-database)
* [sp_delete_database_firewall_rule](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-delete-database-firewall-rule-azure-sql-database)

### **Troubleshooting the database firewall**

If you are seeing that the firewall rules are not behaving as expected, please follow the [recommendations](https://docs.microsoft.com/azure/azure-sql/database/firewall-configure?WT.mc_id=pid%3A13491%3Asid%3A32630421%2F#troubleshoot-the-database-firewall)

## **Recommended Documents**

* [Create and manage firewall rules](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure?WT.mc_id=pid:13491:sid:32630421/)<br>
* [Virtual network endpoints](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview?WT.mc_id=pid:13491:sid:32630421/)<br>
* [Powershell create virtual service endpoint](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-powershell?WT.mc_id=pid:13491:sid:32630421/)
