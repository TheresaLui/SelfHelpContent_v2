<properties
  pagetitle="Connection timeouts"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="katmac"
  selfhelptype="Generic"
  supporttopicids="32637246"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="a22b8b46-2c2b-4518-97c6-5962c1e71be5"
  ownershipid="AzureData_AzureSQLMI" />
# Connection timeouts

Connection timeouts occur when the client application is unable to reach the database. See the [online troubleshooting guide](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-errors-issues) for the most common issues. Check the following:

## **Recommended Steps**

- Verify that firewalls are open
- Ensure routing is configured correctly

### **Run Connectivity Checks Using the Azure SQL Connectivity Checker tool**

To understand the root cause of the connectivity issue between your client and the database, this PowerShell script will run some connectivity checks on your machine to the server to the database. Please upload the output of this script, if you file a support ticket.

To run the script, you need to:

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

4. Set the parameters on the script. Server name is required. Database name, and user and password are optional but desirable.
5. Run the script
6. Review the results in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created. Please send Microsoft all contents of the AllFiles.zip file using the File upload option in the Details tab of the New Support Request in the Support + Troubleshooting section of the Azure Portal.

## **Recommended Documents**

- [Verify the Azure SQL Managed Instance built-in firewall](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-endpoint-verify-built-in-firewall)
- [Troubleshooting connectivity issues and other errors with Microsoft Azure SQL Database and Azure SQL Managed Instance](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database)
- [Working with SQL Database connection issues and transient errors](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)
- [Planning for Azure maintenance events in Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-planned-maintenance)
