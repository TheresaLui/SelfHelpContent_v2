<properties
	pageTitle="Managing database permissions and access"
	description="Managing database permissions and access"
	service="microsoft.sql"
	resource="servers"
	authors="kasparks"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="31980424, 31980425"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="public"
	articleId="3de8d91a-27c4-4cc9-be81-b846ba2da3f3"
/>

# Managing database permissions and access

## **Recommended Steps**
The following details explain how to set up and update common access and permissions rules in Azure SQL Database.

* Change the administrative password for a logical server.<br>
Click "Reset Password" at the top of the SQL Server resource blade.
* Update IP addresses that are authorized to access the server and database.<br>
[How to: Configure firewall settings on SQL Database](https://azure.microsoft.com/documentation/articles/sql-database-configure-firewall-settings/)
* Create contained or isolated database users.<br>
[Contained Database Users - Making Your Database Portable](https://msdn.microsoft.com/library/ff929188.aspx)
* Set up Azure Active Directory-based authentication for contained database users.<br>
[Connecting to SQL Database by using Azure Active Directory Authentication](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/)
* Set up additional users or logins for high privileged access to the master database.<br>
[Managing databases and logins in Azure SQL Database](https://azure.microsoft.com/documentation/articles/sql-database-manage-logins/)

## **Recommended Documents**
[Troubleshoot common Azure SQL Database permissions and access issues](http://azure.microsoft.com/documentation/articles/sql-database-troubleshoot-permissions/)<br>
[Azure SQL Database security guidelines and limitations](http://azure.microsoft.com/documentation/articles/sql-database-security-guidelines/)
