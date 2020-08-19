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

An established connection to SQL Database may be unexpectedly terminated for a variety of reasons.  This could be due to an issue within Azure (maintenance, user-initiated scaling, etc), network issues between the service and client application (including the Internet, internet service providers and on-premise network), or even the client application.  Error messages will vary depending on which client library is used by the application and what layer terminated the connection.  Some of the common errors are:

**Communication Link Failure**<br>
**Connection reset by peer: socket {read | write} error**<br>
**A severe error occurred on the current command.  The results, if any, should be discarded**<br>

## **Recommended Solutions**
- Check [Resource Health](https://docs.microsoft.com/azure/sql-database/sql-database-resource-health?WT.mc_id=pid:13491:sid:32745426/) to quickly determine whether there was an Azure service issue.
- If you are using connection pooling, confirm that you test the connection returned from the pool.  Note that the Azure SQL DB gateway terminate sessions that are idle for longer than a certain period of time, and this frequently impacts pooled connections.  Switch the [Connection policy](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture?WT.mc_id=pid:13491:sid:32745426#connection-policy) for your server from **proxy** to **redirect** to bypass the gateway after connecting.
- The Microsoft [JDBC driver](https://docs.microsoft.com/sql/connect/jdbc/connecting-to-an-azure-sql-database?WT.mc_id=pid:13491:sid:32745426&view=sql-server-ver15) and other third party drivers don't enable TCP KeepAlive, which causes the network layer to drop the connection after a certain idle period.  Verify that you have the latest client drivers installed and that the driver enables KeepAlive.
- Make sure that all production applications have robust [retry logic](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745426#retry-logic-for-transient-errors) to handle dropped connections and transient errors.



### **Azure SQL Connectivity Checker tool**
Because some of these errors involve network configuration, this client-side network connectivity checker can identify common configuration/network issues that may manifest in one of these errors.  This Powershell script is run from the client machine where the error is occurring.

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
- [Common connectivity issues](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues?WT.mc_id=pid:13491:sid:32745426/)<br>
