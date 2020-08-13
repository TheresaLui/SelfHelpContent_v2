<properties
    pageTitle="Connection timeouts"
    description="Connection timeouts"
    service="microsoft.sql"
    resource="servers"
    authors="emlisa"
    ms.author="emlisa"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745425"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="ed58b3a0-20fe-4cb6-a261-5afaa0d4324a-new-st"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Connection timeouts

When you are experiencing connection timeouts, please ensure your application is using a login timeout of at least 15 seconds. Also confirm that the database is not hitting the [limits](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32745425/) of your selected service tier.

### **Azure SQL Connectivity Checker tool**

This PowerShell script will run some connectivity checks from your machine to the server and database.

In order to run it you need to:

<ol>
<li> Open Windows PowerShell ISE in Administrator mode. For the better results, our recommendation is to use the advanced connectivity tests which demand to start PowerShell in Administrator mode. You can still run the basic tests, in case you decide not to run this way. Please note that script parameters 'RunAdvancedConnectivityPolicyTests' and 'CollectNetworkTrace' will only work if the admin privileges are granted.</li><br>

<li> Open a New Script window</li><br>
<li> Paste the following in the script window:

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
</li><br>
<li> Set the parameters on the script, you need to set server name. Database name, user and password are optional but desirable.</li><br>
<li> Run it</li><br>
<li> The results can be seen in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created. Please send us AllFiles.zip using the 'File upload' option in the 'Details' step.</li><br>
</ol>

## **Recommended Documents**

* [Troubleshoot connectivity issues](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database?WT.mc_id=pid:13491:sid:32745425/)<br>
* [SQL Database error codes and corrective actions](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages?WT.mc_id=pid:13491:sid:32745425/)<br>
