<properties
    pageTitle="Dropped connections (Communication link failure, connection reset, etc)"
    description="Dropped connections (Communication link failure, connection reset, etc)"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32746121"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="sqlmi-conn-ts-droppedconnections"
    ownershipId="AzureData_AzureSQLMI"
/>

# Dropped connections, Communication link failure, Connection resets

An established connection to SQL Managed Instance may be unexpectedly terminated for a variety of reasons.  This could be due to an issue within Azure (maintenance, user-initiated scaling, etc), network issues between the service and client application (including the Internet, internet service providers and on-premise network), or even the client application.  Error messages will vary depending on which client library is used by the application and what layer terminated the connection.  Some of the common errors are:

**Communication Link Failure**<br>

**Connection reset by peer: socket {read | write} error**<br>

**A severe error occurred on the current command.  The results, if any, should be discarded**<br>


## **Recommended Steps**
- SQL Managed Instance requires update of client drivers to support the connectivity, here is a list of minimum driver versions required on the client side: 
    - .NET Framework 4.6.1 (or .NET Core)
    - ODBC driver v17
    - PHP driver 5.2.0
    - JDBC driver 6.4.0
    - Node.js driver 2.1.1
    - OLEDB driver 18.0.2.0
    - SSMS 18.0 or higher
    - SMO 150 or higher
- The Azure SQL DB gateway terminate sessions that are idle for longer than 30 minutes.  This frequently impacts pooled, idle connections.  Switch the [Connection type](https://docs.microsoft.com/azure/azure-sql/managed-instance/connection-types-overview) for your server from **proxy** to **redirect**, which bypasses the gateway once connected, eliminating this issue.
- The Microsoft JDBC driver and some other third party drivers don't enable TCP KeepAlive, which causes the TCP network layer to drop the connection after a certain idle period.  Verify that you have the latest client drivers installed and that the driver enables [KeepAlive](https://docs.microsoft.com/en-us/sql/connect/jdbc/connecting-to-an-azure-sql-database?view=sql-server-ver15#connections-dropped).
- Make sure that all production applications have robust [retry logic](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors) to handle dropped connections and transient errors.



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

- [Troubleshooting connectivity issues and other errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-errors-issues/)
- [Working with transient connectivity errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues/)
