<properties
    pageTitle="Connection timeouts"
    description="Connection timeouts"
    infoBubbleText="Connection timeouts"
    service=""
    resource=""
    authors="srdan-bozovic-msft"
    ms.author="srbozovi"
    displayOrder=""
    articleId="a22b8b46-2c2b-4518-97c6-5962c1e71be5"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32637246"
    resourceTags=""
    productPesIds="16259"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    ownershipId="AzureData_AzureSQLMI"
/>

# Connection timeouts

## **Recommended Steps**

- Check if firewalls are open
- Check if routing is configured properly

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

## **Recommended Documents**

- [Troubleshooting connectivity issues and other errors with Microsoft Azure SQL Database](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database)
- [Working with SQL Database connection issues and transient errors](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)
- [Planning for Azure maintenance events in Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-planned-maintenance)
