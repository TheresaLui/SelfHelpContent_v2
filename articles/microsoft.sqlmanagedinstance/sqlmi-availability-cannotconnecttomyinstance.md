<properties
    pageTitle="Cannot connect to my instance"
    description="Cannot connect to my instance"
    infoBubbleText="Cannot connect to my instance"
    service=""
    resource=""
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder=""
    articleId="sqlmi-availability-cannotconnecttomyinstance"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739488"
    resourceTags=""
    productPesIds="16259"
    cloudEnvironments="public"
    ownershipId="AzureData_AzureSQLMI"
/>

# Cannot connect to my instance

## **Recommended Steps**

- Check if firewalls are open
- Check if routing is configured properly

### Error 10928: The session limit for the database is X and has been reached

* The Resource ID indicates which resource governance limit is being hit. A value of 1 is a limit on worker threads; 2 is a limit on sessions (connections). For short term mitigation, increase the [service tier](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32630429/) of your database; longer term, tune the workload so it better fits the selected tier. Refer to the [Query Performance Insight](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32630429/) feature for assistance analyzing and tuning your workload. <br>

### Error 18456: Login failed for user X

* Troubleshoot this error using the [Azure SQL Database Connectivity troubleshooter](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#unable-to-log-in-to-the-server-errors-18456-40531?WT.mc_id=pid:13491:sid:32630429/) <br>

### Error 40613: Database X on server Y is not currently available

* This common, transient error occurs when you database is undergoing a reconfiguration, and normally lasts less than 60 seconds. [Read more](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database#transient-fault-error-messages-40197-40613-and-others?WT.mc_id=pid:13491:sid:32630429/) about how to handle this. <br>

### Login/connection timeouts

* Ensure your application is using a login timeout of at least 15 seconds. Also confirm that the database is not hitting the [limits](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32630429/) of your selected service tier.

### Other error not listed

* [Troubleshooting connectivity issues and other errors with Microsoft Azure SQL Database](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database)
* [Working with SQL Database connection issues and transient errors](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)
* [Connect your application to Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-connect-app)

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