<properties
	pageTitle="Azure SQL Data Sync Health Checker"
	description="Azure SQL Data Sync Health Checker"
	infoBubbleText="Azure SQL Data Sync Health Checker"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_healthchecker"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>

# Azure SQL Data Sync Health Checker

<!--issueDescription-->
We have a tool called Azure SQL Data Sync Health Checker. This PowerShell script will check if all the metadata of a hub and member is in place and also validate the scopes against the information we have on the sync metadata database (among other validations). This script will not make any changes, will just validate data sync and user objects. It will also gather some useful information for faster troubleshooting.
<!--/issueDescription-->

## **Recommended Steps**

If you run this test, please submit the results during case submission:

1. Open Windows PowerShell ISE
2. Open a New Script window
3. Paste the following in the script window (please note that except databases and credentials, the other parameters are optional):

  ```
    $parameters = @{
        ## Databases and credentials
        # Sync metadata database credentials (Only SQL Authentication is supported)
        SyncDbServer = '<!--$HealthCheckerSyncDBServer-->HealthCheckerSyncDBServer<!--/$HealthCheckerSyncDBServer-->.database.windows.net'
        SyncDbDatabase = '<!--$HealthCheckerSyncDBDatabase-->HealthCheckerSyncDBDatabase<!--/$HealthCheckerSyncDBDatabase-->'
        SyncDbUser = ''
        SyncDbPassword = ''

        # Hub credentials (Only SQL Authentication is supported)
        HubServer = '.database.windows.net'
        HubDatabase = ''
        HubUser = ''
        HubPassword = ''

        # Member credentials (Azure SQL DB or SQL Server)
        MemberServer = ''
        MemberDatabase = ''
        MemberUser = ''
        MemberPassword = ''
        # set MemberUseWindowsAuthentication to $true in case you wish to use integrated Windows authentication (MemberUser and MemberPassword will be ignored)
        MemberUseWindowsAuthentication = $false
    }

    $scriptUrlBase = 'https://raw.githubusercontent.com/Microsoft/AzureSQLDataSyncHealthChecker/master'
    Invoke-Command -ScriptBlock ([Scriptblock]::Create((iwr ($scriptUrlBase+'/AzureSQLDataSyncHealthChecker.ps1')).Content)) -ArgumentList $parameters
    #end
  ```

4. Set the parameters on the script: you need to set server names, database names, users, and passwords
5. Run it
6. The major results can be seen in the output window

If the user has the permissions to create folders, a folder with all the resulting files will be created. When running on Windows, the folder will be opened automatically after the script completes. When running on Azure Portal Cloud Shell the files will be stored in the file share (clouddrive). A zip file with all the files (AllFiles.zip) will be created.

Please send us AllFiles.zip or the log from the output window in a text file. You will have the chance to upload files in the Details phase of the case submission.

More details can be found at https://github.com/Microsoft/AzureSQLDataSyncHealthChecker.
