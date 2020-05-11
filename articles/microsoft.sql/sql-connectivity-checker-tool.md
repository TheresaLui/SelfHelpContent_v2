<properties
    pageTitle="Azure SQL Connectivity Checker tool"
    description="Azure SQL Connectivity Checker tool"
    infoBubbleText="Azure SQL Connectivity Checker tool its a PowerShell script to run some connectivity checks from customers machine."
    service="microsoft.sql"
    resource="servers"
    ms.author="vitomaz"
    authors="vitomaz-msft"
    displayOrder=""
    articleId="sql-connectivity-checker-tool"
    diagnosticScenario="SqlConnectivityCheckerTool"
    selfHelpType="diagnostics"
    supportTopicIds="32630429"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Azure SQL Connectivity Checker
<!--issueDescription-->
This PowerShell script will run some connectivity checks from this machine to the server and database.
<!--/issueDescription-->

## **Recommended Steps**

If you run this test, please submit the results during case submission:

1. Open Windows PowerShell ISE in Administrator mode. Administrator privileges are required to 'RunAdvancedConnectivityPolicyTests' and 'CollectNetworkTrace'. In case you cannot run in administrator mode please continue, the tool will still run relevant tests.
2. Open a New Script window
3. Paste the following in the script window:

```
$parameters = @{
    Server = '.database.windows.net'
    Database = ''  # Set the name of the database you wish to test, 'master' will be used by default if nothing is set
    User = ''  # Set the login username you wish to use, 'AzSQLConnCheckerUser' will be used by default if nothing is set
    Password = ''  # Set the login password you wish to use, 'AzSQLConnCheckerPassword' will be used by default if nothing is set

    ## Optional parameters (default values will be used if ommited)
    SendAnonymousUsageData = $true  # Set as $true (default) or $false
    RunAdvancedConnectivityPolicyTests = $true  # Set as $true (default) or $false, this will download the library needed for running advanced connectivity tests
    CollectNetworkTrace = $true  # Set as $true (default) or $false
    #EncryptionProtocol = '' # Supported values: 'Tls 1.0', 'Tls 1.1', 'Tls 1.2'; Without this parameter operating system will choose the best protocol to use
}

$ProgressPreference = "SilentlyContinue";
$scriptUrlBase = 'raw.githubusercontent.com/Azure/SQL-Connectivity-Checker/master'
Invoke-Command -ScriptBlock ([Scriptblock]::Create((iwr ($scriptUrlBase+'/AzureSQLConnectivityChecker.ps1')).Content)) -ArgumentList $parameters
#end
```

4. Set the parameters on the script, you need to set server name. Database name, user and password are optional but desirable.
5. Run it
6. The results can be seen in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created.

More details can be found at https://github.com/Azure/SQL-Connectivity-Checker.
