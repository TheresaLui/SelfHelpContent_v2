<properties
	pageTitle="Connection issues to SQL Azure DB"
	description="Connection issues to SQL Azure DB"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="31980428, 31980412, 31980414, 31980421"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
	articleId="019b47bd-d8fc-4e7e-86b3-e6a35d44ad50"
/>

# Connection issues to SQL Azure DB

## **Recommended Steps**

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string, and other causes.

* [Configure SQL Azure firewall rules](https://docs.azure.cn/sql-database/sql-database-configure-firewall-settings/)
to allow the client IP address
* Follow [Connection recommendations](https://azure.microsoft.com/documentation/articles/sql-database-connect-central-recommendations/#connection-recommendations) on computers that host your client program<br>
* Fix incorrect [connection strings to Azure SQL Database](https://docs.azure.cn/sql-database/sql-database-connectivity-issues/#connections-to-azure-sql-database) in your application.<br>

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure SQL Database](https://docs.azure.cn/sql-database/sql-database-troubleshoot-common-connection-issues/)<br>
* [Connecting to SQL Database: Best Practices and Design Guidelines](https://docs.azure.cn/sql-database/sql-database-troubleshoot-common-connection-issues/)
