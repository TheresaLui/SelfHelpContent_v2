<properties
	pageTitle="Managing database permissions and access"
	description="Managing database permissions and access"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="11"
	selfHelpType="resource"
	supportTopicIds="31980424, 31980425"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
	articleId="048ac2e0-d5d9-41ae-b5c0-931dadd3368c"
/>

# Managing database permissions and access

## **Recommended Steps**

The following details explain how to set up and update common access and permissions rules in Azure SQL Database.

* Change the administrative password for a logical server by clicking "Reset Password" at the top of the SQL Server resource blade
* [Configure firewall settings on SQL Database](https://docs.azure.cn/sql-database/sql-database-configure-firewall-settings/) and update IP addresses that are authorized to access the server and database
* Create [contained](https://msdn.microsoft.com/library/ff929188.aspx) or isolated database users
* Set up [Azure Active Directory Authentication](https://docs.azure.cn/sql-database/sql-database-aad-authentication/) for contained database users
* Set up [additional users or logins](https://docs.azure.cn/sql-database/sql-database-manage-logins/) for high privileged access to the master database

## **Recommended Documents**

* [Troubleshoot common Azure SQL Database permissions and access issues](http://docs.azure.cn/sql-database/sql-database-troubleshoot-permissions/)<br>
* [Azure SQL Database security guidelines and limitations](http://docs.azure.cn/sql-database/sql-database-security-guidelines/)
