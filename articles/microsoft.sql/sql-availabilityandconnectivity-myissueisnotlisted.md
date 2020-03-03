<properties
	pageTitle="availability and connectivity/my issue is not listed"
	description="availability and connectivity/my issue is not listed"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32630439"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	articleId="8d4208f6-e85a-4928-99e6-252b5baf39ca"
	ownershipId="AzureData_AzureSQLDB"
/>

# Availability and Connectivity/my issue is not listed

## **Recommended Steps**

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string, and other causes. <br>

* Set up [firewall rules](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure) to allow the client IP address
* Follow [Connection recommendations](https://docs.microsoft.com/azure/sql-database/sql-database-develop-overview#connection-recommendations?WT.mc_id=pid:13491:sid:32630439/) on computers that host your client program<br>
* Fix incorrect [Connection strings to Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#connections-to-azure-sql-database?WT.mc_id=pid:13491:sid:32630439?WT.mc_id=pid:13491:sid:32630439/) in your application

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure SQL Database](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#steps-to-fix-common-connection-issues?WT.mc_id=pid:13491:sid:32630439/)<br>
