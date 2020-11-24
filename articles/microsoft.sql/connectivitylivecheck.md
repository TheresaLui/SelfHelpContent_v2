<properties
  pageTitle="Connectivity Live Check"
  description="Connectivity Live Check"
  infoBubbleText="Found recent connectivity issue. See details on the right."
  service="microsoft.sql"
  resource="servers"
  authors="subbu-kandhaswamy, swbhartims"
  ms.author="subbuk, swbharti"
  displayOrder=""
  articleId="ConnectivityCheck_042F9ACD-6B75-4184-A72C-A7F68E71C9B3"
  diagnosticScenario="crc_sqldb_connectivity"
  selfHelpType="diagnostics"
  supportTopicIds="32630429"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We performed a live connectivity check, using mock username/password, against database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->.<!--$ServerNameSuffix-->ServerNameSuffix<!--/$ServerNameSuffix-->, and confirmed <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> is online and processing logins.
<!--/issueDescription-->

The issue you are experiencing could also be a network-related problem on your end.

## **Recommended Steps**

* Try connecting to the database using a different machine to help eliminate the possibility of a machine-specific issue
* Connect to the database from a different network to determine if this is network-related
* Try connecting to the database from a different client
* Contact your network administrator to further investigate the issue on your end

Running the **Azure SQL Connectivity Checker tool** may help to narrow down the potential causes of failure.

This PowerShell script is run from the client machine where the error is occurring.

<ol>
<li> Open Windows PowerShell ISE in Administrator mode. For the better results, we recommend using advanced connectivity tests that require starting PowerShell in Administrator mode. You can still run the basic tests, in case you decide not to run this way. Note that script parameters `RunAdvancedConnectivityPolicyTests` and `CollectNetworkTrace` will only work if the admin privileges are granted.</li><br>

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
<li> Set the parameters on the script. You must set the server name. Database name, user, and password are optional, but best practices.</li><br>
<li> Run it<br>
You can see the results in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created. </li><br>
<li> Check if the tool outputted any recommended action based on test results.</li><br>
</ol>

## **Recommended Documents**

* [Azure SQL Database and Azure Synapse Analytics connectivity architecture](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture)

* [Ports beyond 1433 for ADO.NET 4.5](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports)
