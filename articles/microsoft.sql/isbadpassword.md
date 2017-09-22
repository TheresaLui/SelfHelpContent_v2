<properties
	pageTitle="Database Connectivity issue due to invalid credentials detected"
	description="IsBadPassword"
	infoBubbleText="Found recent login failure. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="aamalvea"
	displayOrder=""
	articleId="IsBadPassword_FED3BCD4-BE62-45F4-9B0F-C8D8CFFDABD5"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Connections attempts to your database <!--$DBName--> Database Name <!--/$DBName--> have failed over the last <!--$NumberofHours--> NumberofHours<!--/$NumberofHours--> hours due invalid credentials. To resolve this issue, contact the service administrator for valid credentials. If this problem persists, share these troubleshooting steps with your service administrator.
<!--/issueDescription-->

Typically, the service administrator can use the following steps to add the login:<br> 
1. Login to the server using SQL Server Management Studio (SSMS).<br> 
2. Check whether the login name is disabled by using the following SQL query:<br> 
```SQL
SELECT name, is_disabled FROM sys.sql_logins
```
<br> 
3. If the corresponding name is disabled, enable it by using the following statement:<br> 
```SQL
Alter login <User name> enable
```
<br> 
4. If the SQL login user name does not exist, create it by using SSMS. To do this, follow these steps:<br> 
	1. Double-click **Security** to expand it.<br> 
	2. Right-click **Logins**, and then select **New login**.<br> 
	3. In the generated script with placeholders, you can edit and run the following SQL query:<br> 
	```SQL
	CREATE LOGIN <SQL_login_name, sysname, login_name>
	WITH PASSWORD = ‘<password, sysname, Change_Password>’
	GO
	```
	<br> 
5. Double-click **Database**.<br> 
6. Select the database to which you want to grant user the permission.<br> 
7. Double-click **Security**.<br> 
8. Right-click **Users**, and then select **New User**.<br> 
9. In the generated script with placeholders, you can edit and run the following SQL query:<br> 
```SQL
CREATE USER <user_name, sysname, user_name>          
FOR LOGIN <login_name, sysname, login_name>
WITH DEFAULT_SCHEMA = <default_schema, sysname, dbo>
GO

-- Add user to the database owner role
EXEC sp_addrolemember N’db_owner’, N’<user_name, sysname, user_name>’
GO      
```
<br> 
**Note** that you can also use `sp_addrolemember` to map specific users to specific database roles.<br> 

For more information, refer to [Managing Databases and Logins in Azure SQL Database](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-manage-logins)

