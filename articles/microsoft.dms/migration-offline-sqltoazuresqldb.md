<properties
	pageTitle="Errors for SQL Server to Azure SQLDB offline migration"
	description="Top 5 migration errors, what it means and what customer can do for SQL Server to Azure SQLDB offline migration"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="ajaykar"
	displayOrder="1"
	articleId="migration-offline-sqltoazuresqldb"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32615126"
	resourceTags=""
	productPesIds="16307"​
	cloudEnvironments="public"
/>

# <-- Errors you may encounter while migrating from SQL Server to Azure SQLDB using offline migration --> 

## **Top Errors - SQL Server to Azure SQLDB offline migration**

1. Could not start the scenario 'StartAzureSqlDbMigrationScenario' as an exception occurred while deserializing the input.<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>What it means:</b> If you hit this error it means that you provided a bad input through PowerShell.<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>What you can do:</b> Please review the input you provided. <br>
<br>
2. Error 4060 - Login failed.<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>What it means:</b> Authentication failed with the target database.<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>What you can do:</b> Review user actions in <a href="https://docs.microsoft.com/en-us/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-2017">Authentication Errors Page</a> and take appropriate action. <br>
<br>
3. This is a step with a link to a blade.<br>
[This is a link to a blade](data-blade:extensionName.bladeName.nameOfInputParam.valueOfInputParam)
4. This is a step with no link, blade, or instructions. Note that because the next line is a new bullet in the numbered list, no <br> is needed.
5. This is a step with code :<br>
```
SELECT name, is_disabled FROM sys.sql_logins
```

## **Recommended documents**

[This is the display text of an external document](https://)<br>
[This is the display text for the last article in the list](http://)
