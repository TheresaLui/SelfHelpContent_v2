<properties
	pageTitle="availability and connectivity/my issue is not listed"
	description="availability and connectivity/my issue is not listed"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    authorAlias="emlisa"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32630439"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>

# Availability and Connectivity/my issue is not listed

## **Recommended steps**

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string and other causes.

* Set up firewall rules to allow the client IP address.<br>
[Configure SQL Azure firewall rules](https://azure.microsoft.com/documentation/articles/sql-database-configure-firewall-settings/)
* Follow connection recommendations on computers that host your client program<br>
[Connection recommendations](https://azure.microsoft.com/documentation/articles/sql-database-connect-central-recommendations/#connection-recommendations)
* Fix incorrect connection strings in your application.<br>
[Connection strings to Azure SQL Database](https://azure.microsoft.com/documentation/articles/sql-database-connectivity-issues/#connections-to-azure-sql-database)

## **Recommended documents**
* [Troubleshoot common connectivity issues to Azure SQL Database](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-common-connection-issues/)<br>
* [Connecting to SQL Database: Best Practices and Design Guidelines](https://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-common-connection-issues/)
