<properties
	pageTitle="availability and connectivity/other issue not listed"
	description="availability and connectivity/other issue not listed"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32628803"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
	articleId="ed1aaaa4-1761-4969-bdeb-c4b449b052b0"
/>

# Availability and Connectivity/other

## **Recommended Steps**

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string, and other causes.

* [Configure SQL Azure firewall rules](https://docs.azure.cn/sql-database/sql-database-configure-firewall-settings/)
to allow the client IP address
* Follow [Connection recommendations](https://azure.microsoft.com/documentation/articles/sql-database-connect-central-recommendations/#connection-recommendations) on computers that host your client program<br>
* Fix incorrect [connection strings to Azure SQL Database](https://docs.azure.cn/sql-database/sql-database-connectivity-issues/#connections-to-azure-sql-database) in your application.<br>

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure SQL Database](https://docs.azure.cn/sql-database/sql-database-troubleshoot-common-connection-issues/)<br>
* [Connecting to SQL Database: Best Practices and Design Guidelines](https://docs.azure.cn/sql-database/sql-database-troubleshoot-common-connection-issues/)
