<properties
	pageTitle="Data Sync failed to connect to the server requested by the login"
	description="Data Sync failed to connect to the server requested by the login due to firewall"
	infoBubbleText="Data Sync failed to connect to the server requested by the login due to firewall"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_firewall"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Data Sync failed to connect to the server

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
Data Sync feature relies on Azure hosted sync agents to perform tasks like Refresh Schema, Provisioning, etc. Those agents need to connect to your databases using Azure IPs. When using Data Sync feature you need to keep **Allow access to Azure services** turned on so the sync agents can access your SQL Database server. Alternatively, you can just whitelist the SQL DB IP Ranges for hub's region.<br>

Data Sync was not able to reach the following database(s):<br>

**<!--$FirewallClosedDatabaseList--> FirewallClosedDatabaseList <!--/$FirewallClosedDatabaseList-->**

<!--/issueDescription-->

## **Recommended Steps**

To turn on the **Allow access to Azure services** server-level IP firewall rule in the [Azure Portal](https://portal.azure.com), you can either go to the Overview page for your Azure SQL database or the Overview page for your SQL Database server.

* To set a server-level IP firewall rule from the database overview page:

	1. Click **Set server firewall** on the toolbar, the firewall settings page for the SQL Database server opens
	2. Set **Allow access to Azure services** to **ON** and then click **Save**
	3. It may take up to five minutes for this change to take effect

* To set a server-level rule from server overview page:

	1. Click **Firewall** in the left-hand menu under Settings
	2. Set **Allow access to Azure services** to **ON** and then click **Save**
	3. It may take up to five minutes for this change to take effect

* Using T-SQL you can connect to the **master** database of the server and run the following command:

```
EXECUTE sp_set_firewall_rule @name = N'AllowAllWindowsAzureIps',
   @start_ip_address = '0.0.0.0', @end_ip_address = '0.0.0.0'
```

* Alternatively, you can whitelist the SQL DB IP Ranges for hub's region. You can find the ranges for each region at:

	* [Azure IP Ranges and Service Tags – Public Cloud](https://www.microsoft.com/download/details.aspx?id=56519)
	* [Azure IP Ranges and Service Tags – China Cloud](https://www.microsoft.com/download/details.aspx?id=57062)
	* [Azure IP Ranges and Service Tags – Germany Cloud](https://www.microsoft.com/download/details.aspx?id=57064)
	* [Azure IP Ranges and Service Tags – US Government Cloud](https://www.microsoft.com/download/details.aspx?id=57063)

**Note:** Enabling Allow access to Azure services in national clouds or government clouds will not open the public cloud ranges, and vice-versa.

## **Recommended Documents**

* [Azure SQL Database IP firewall rules](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure/)
