<properties
    pageTitle="Azure SQL Connectivity Checker tool"
    description="Azure SQL Connectivity Checker tool"
    infoBubbleText="Azure SQL Connectivity Checker tool its a PowerShell script to run some connectivity checks from customers machine."
    service="microsoft.sql"
    resource="servers"
    ms.author="vitomaz"
    authors="vitomaz-msft"
    displayOrder=""
    articleId="sql-connectivity-checker-tool-new-st"
    diagnosticScenario="SqlConnectivityCheckerTool"
    selfHelpType="diagnostics"
    supportTopicIds="32745425"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Azure SQL Connectivity Checker
<!--issueDescription-->
Running the **Azure SQL Connectivity Checker tool** may help to narrow down the potential causes of failure.
<!--/issueDescription-->

## **Recommended Steps**

This PowerShell script is run from the client machine where the error is occurring.

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
<li> Run it<br>
 The results can be seen in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created. </li><br>
<li> Check if the tool outputted any recommended action based on test results.</li><br>
</ol>

More details can be found at https://github.com/Azure/SQL-Connectivity-Checker.
