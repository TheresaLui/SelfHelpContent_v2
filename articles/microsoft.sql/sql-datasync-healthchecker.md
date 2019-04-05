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
	supportTopicIds="32574329"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
/>
# Azure SQL Data Sync Health Checker

We have a tool called Azure SQL Data Sync Health Checker. This PowerShell script will check if all the metadata of a hub and member is in place and also validate the scopes against the information we have on the sync metadata database (among other validations). This script will not make any changes, will just validate data sync and user objects. It will also gather some useful information for faster troubleshooting.
You can check all the details at https://github.com/vitomaz-msft/DataSyncHealthChecker
Can you please run it and send us the results? 

**In order to run it you need to:**

1. Open Windows PowerShell ISE

2. Open a New Script window

3. Paste the following in the script window (please note that, except databases and credentials, the other parameters are optional):

```powershell
$parameters = @{
    ## Databases and credentials
    # Sync metadata database credentials (Only SQL Authentication is supported)
    SyncDbServer = '.database.windows.net'
    SyncDbDatabase = ''
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
 
$scriptUrlBase = 'https://raw.githubusercontent.com/vitomaz-msft/DataSyncHealthChecker/master'

Invoke-Command -ScriptBlock ([Scriptblock]::Create((iwr ($scriptUrlBase+'/Data%20Sync%20Health%20Checker.ps1')).Content)) -ArgumentList $parameters
#end
```

4. Set the parameters on the script, you need to set server names, database names, users and passwords.

5. Run it.

6. The major results can be seen in the output window. 
If the user has the permissions to create folders, a folder with all the resulting files will be created.
When running on Windows, the folder will be opened automatically after the script completes.
When running on Azure Portal Cloud Shell the files will be stored in the file share (clouddrive).
A zip file with all the files (AllFiles.zip) will be created.
Please send us AllFiles.zip or the log from the output window in case user cannot write files.