<properties
    pageTitle="Dropped connections, Communication link failure, Connection resets"
    description="Dropped connections, Communication link failure, Connection resets"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745426"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="4D25AD8C-6278-444B-91ED-C99664A0389E"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Dropped connections, Communication link failure, Connection resets

* SQL Azure requires connections over the internet or other complex networks and because of this, you should be prepared to handle unexpected dropping of connections. Established connections consist of: connections that are returning data, open connections in the connection pool, or connections being cached in client side variables. When you are connecting to SQL database, connection loss is a valid scenario that you need to plan for in your code. The best way to handle connection loss it to re-establish the connection and then re-execute the failed commands or query.

* The quality of all network components between the machine running your client code and the SQL DB Servers is at times outside of Microsoft’s sphere of control.  There are many number of reasons that may result in the disconnection of your sessions. In circumstances when you encounter network problem causing disconnections, please use the below connectivity checker tool to identify the problematic behavior.

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

- [Troubleshooting connectivity issues with Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-errors-issues?WT.mc_id=pid:13491:sid:32745426/)
- [Common connectivity issues](https://docs.microsoft.com/en-us/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745426/)<br>
