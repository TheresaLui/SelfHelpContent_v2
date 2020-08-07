<properties
    pageTitle="Database X on server Y is not currently available"
    description="Database X on server Y is not currently available"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745430"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="E8D094DB-9BC4-40D3-8C7A-41CD46189C84"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Database X on server Y is not currently available

## **Recommended Steps**

### Error 40613: Database X on server Y is not currently available

* This common, transient error occurs when you database is undergoing a reconfiguration, and normally lasts less than 60 seconds. [Read more](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#transient-fault-error-messages-40197-40613-and-others?WT.mc_id=pid:13491:sid:32745425/) about how to handle this. <br>

### **Azure SQL Connectivity Checker tool**

This PowerShell script will run some connectivity checks from your machine to the server and database.

In order to run it you need to:

1. Open Windows PowerShell ISE in Administrator mode. For the better results, our recommendation is to use the advanced connectivity tests which demand to start PowerShell in Administrator mode. You can still run the basic tests, in case you decide not to run this way. Please note that script parameters 'RunAdvancedConnectivityPolicyTests' and 'CollectNetworkTrace' will only work if the admin privileges are granted.

2. Open a New Script window
3. Paste the following in the script window:

```
    $parameters = @{
        Server = '.database.windows.net'
        Database = ''  # Set the name of the database you wish to test, 'master' will be used by default if nothing is set
        User = ''  # Set the login username you wish to use, 'AzSQLConnCheckerUser' will be used by default if nothing is set
        Password = ''  # Set the login password you wish to use, 'AzSQLConnCheckerPassword' will be used by default if nothing is set

        ## Optional parameters (default values will be used if omitted)
        SendAnonymousUsageData = $true  # Set as $true (default) or $false
        RunAdvancedConnectivityPolicyTests = $true  # Set as $true (default) or $false, this will load the library from Microsoft's GitHub repository needed for running advanced connectivity tests
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
6. The results can be seen in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created. Please send us AllFiles.zip using the 'File upload' option in the 'Details' step.
