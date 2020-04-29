<properties
	pageTitle="SQL Agent, Messaging and queuing/SQL Server Agent"
	description="SQL Server Agent/Assistance on questions or issues related to SQL Server Agent"
	service="microsoft.sql"
	resource="sqlAgent"
	authors="misliplavo"
    ms.author="mlazic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId=""
	ownershipId="AzureData_AzureSQLMI"
/>

# Sql Server Agent
[Sql Server Agent](https://docs.microsoft.com/sql/ssms/agent/sql-server-agent?view=sql-server-ver15) is a Microsoft Windows service that executes scheduled administrative tasks, which are called jobs in SQL Server 2019 (15.x).

## **Recommended Steps**

If you are experiencing some issues with Sql Server Agent, some of the following steps might help you to troubleshoot the issues:

**I cannot see my SQL Server Agent node in Object explorer**
There are three fixed DB SqlServer Agent roles:
•	SQLAgentUserRole
•	SQLAgentReaderRole
•	SQLAgentOperatorRole
When users who are not members of one of these roles are connected to SQL Server in SQL Server Management Studio, the SQL Server Agent node in Object Explorer is not visible. A user must be a member of one of these fixed database roles or a member of the sysadmin fixed server role to use SQL Server Agent.
[SQL Agent fixed database roles](https://docs.microsoft.com/sql/ssms/agent/sql-server-agent-fixed-database-roles?view=sql-server-ver15)

**I’m getting "The EXECUTE permission was denied on the object <object_name> (Microsoft SQL Server, Error: 229)" error**
Each of the logins added to SQL Agent fixed database roles needs to explicitly grant EXECUTE permissions to the stored procedures listed below. 
`USE [master]`
`GO`
`CREATE USER [login_name] FOR LOGIN [login_name]`
`GO`
`GRANT EXECUTE ON master.dbo.xp_sqlagent_enum_jobs TO [login_name]`
`GRANT EXECUTE ON master.dbo.xp_sqlagent_is_starting TO [login_name]`
`GRANT EXECUTE ON master.dbo.xp_sqlagent_notify TO [login_name]`
 
[SQL Agent roles need explicit EXECUTE permissions for non-sysadmin logins](https://docs.microsoft.com/azure/sql-database/sql-database-release-notes?tabs=managed-instance#sql-agent-roles-need-explicit-execute-permissions-for-non-sysadmin-logins)

**How can I disable my Sql Server Agent?**
For managed instance enabling and disabling of SQL Server Agent is currently not supported. SQL Agent is always running.


## **Recommended Documents**

- [Managed instance T-SQL differences and limitations (Sql Server Agent)](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent)
- [SQL Agent roles need explicit EXECUTE permissions for non-sysadmin logins](https://docs.microsoft.com/azure/sql-database/sql-database-release-notes?tabs=managed-instance#in-memory-oltp-memory-limits-are-not-applied)

