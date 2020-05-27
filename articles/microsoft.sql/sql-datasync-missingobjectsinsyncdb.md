<properties
	pageTitle="Data Sync objects are missing from Sync Metadata database"
	description="We were able to detect that Data Sync related objects are missing from Sync Metadata database"
	infoBubbleText="We were able to detect that Data Sync related objects are missing from Sync Metadata database"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_missingobjectsinsyncdb"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>

# Data Sync related objects are missing from Sync Metadata database

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect that Data Sync related objects are missing from Sync Metadata database. Data Sync cannot run without these objects. The error message **<!--$SyncDBErrorMessage--> SyncDBErrorMessage <!--/$SyncDBErrorMessage-->** was detected on the sync metadata database <!--$SyncDBServer--> SyncDBServer <!--/$SyncDBServer-->/<!--$SyncDBDatabase--> SyncDBDatabase <!--/$SyncDBDatabase-->.
<!--/issueDescription-->

This is a situation we cannot usually recover from, and requires your sync account to be cleaned from the backend so you can start from scratch.<br>

## **Recommended Steps**

In case you are aware that the objects were removed from your database, please proceed with the support request submission and let us know if we can remove all your sync groups and sync agents in this region from the Azure backend in the details section.

If you are unsure about the missing objects, run the PowerShell script below from either Windows PowerShell or Azure Cloud Shell and share the results with us. You will need to fill the SyncDbUser and the SyncDbPassword parameters. This script will check the missing objects from Sync Metadata Database. Based on the missing objects, we will provide you an action plan.

```
$parameters = @{    
    SyncDbServer = '<!--$SyncDBServer--> SyncDBServer <!--/$SyncDBServer-->.database.windows.net'
    SyncDbDatabase = '<!--$SyncDBDatabase--> SyncDBDatabase <!--/$SyncDBDatabase-->'
    SyncDbUser = ''
    SyncDbPassword = ''
}

$scriptUrlBase = 'https://raw.githubusercontent.com/Microsoft/AzureSQLDataSyncHealthChecker/master/AzureSQLDataSyncHealthChecker.ps1'
Invoke-Command -ScriptBlock ([Scriptblock]::Create((iwr ($scriptUrlBase)).Content)) -ArgumentList $parameters
#end
```

### Disclaimers

These scripts are copyright Microsoft Corporations and are provided as samples. They are not part of any Azure service and are not covered by any SLA or other Azure-related agreements. They are provided as-is with no warranties express or implied. Microsoft takes no responsibility for the use of the scripts or the accuracy of this document. Familiarize yourself with the scripts before using them.
