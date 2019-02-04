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
	supportTopicIds="32574329"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We were able to detect that Data Sync related objects are missing from Sync Metadata database, Data Sync cannot run without this objects.<br>
The error message **<!--$SyncDBErrorMessage--> SyncDBErrorMessage <!--/$SyncDBErrorMessage-->** was detected on the sync metadata database <!--$SyncDBServer--> SyncDBServer <!--/$SyncDBServer-->/<!--$SyncDBDatabase--> SyncDBDatabase <!--/$SyncDBDatabase-->
<!--/issueDescription-->

This is usually a situation we cannot recover from and requires your sync account to be cleaned from the backend so you can start from scratch.<br>

## **Recommended Steps**

In case you are aware that the objects were removed from your database please proceed with the support request submission and let us know if you can remove all the sync groups and sync agents from the Azure backend in the details section.

If you unsure about the missing objects, run the script below from either Windows or Azure Cloud Shell and share the results with us.
This script will check the missing objects from Sync Metadata Database.
Based on the missing objects we will provide you an action plan.

```powershell

$parameters = @{    
    SyncDbServer = '<!--$SyncDBServer--> SyncDBServer <!--/$SyncDBServer-->.database.windows.net'
    SyncDbDatabase = '<!--$SyncDBDatabase--> SyncDBDatabase <!--/$SyncDBDatabase-->'
    SyncDbUser = '<username>'
    SyncDbPassword = '<password>'
}

$scriptUrlBase = 'https://raw.githubusercontent.com/vitomaz-msft/DataSyncHealthChecker/master/Data%20Sync%20Health%20Checker.ps1'
Invoke-Command -ScriptBlock ([Scriptblock]::Create((iwr ($scriptUrlBase)).Content)) -ArgumentList $parameters

```

## Disclaimers
This scripts are copyright Microsoft Corporations and are provided as samples. They are not part of any Azure service and are not covered by any SLA or other Azure-related agreements. They are provided as-is with no warranties express or implied. Microsoft takes no responsibility for the use of the scripts or the accuracy of this document. Familiarize yourself with the scripts before using them.