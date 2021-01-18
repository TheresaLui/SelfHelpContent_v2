<properties
pageTitle="Other connectivity errors not listed"
description="Other connectivity errors not listed"
ms.author="vimahadi"
displayOrder=""
articleId="444c93f4-7604-4360-b1c0-613d1f7ab738"
selfHelpType="Apollo"
supportTopicIds="4c94cc3b-8a64-54e9-0582-287ac46d9504"
productPesIds="13491"
cloudEnvironments="public"
ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Troubleshoot most common SQL Db connectivity issues

## Troubleshoot most common SQL Db connectivity issues
:::Section Insights:::

Connection problems can be caused by multiple reasons like reconfiguration, firewall settings, connection timeouts, login failures, resource limits, network specific issues and failure to apply best practices and guidelines during your client application design. 
If you are experiencing connection failures outside of the above scenarios then insights from diagnostics, and running the Connectivity Checker tool can help to narrow down the potential causes of failure.

### SQL Db connectivity diagnostics

<Insight>
    <symptomId>SqlLtsFailedLogin,SqlConnectivity,SqlCustomerVerbatims,SqlLts,SqlConnectivityBasic</symptomId>
    <executionText>The diagnostic is running some checks on your resource</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText> 
    <noResultText>The diagnostic did not find any issues. Use the troubleshooting steps below to resolve your problem</noResultText>
    <additionalInputsReq>true</additionalInputsReq> 
    <maxInsightCount>2</maxInsightCount>
</Insight>

### Azure SQL Connectivity Checker tool

This PowerShell script will run connectivity checks from your machine to the server and database.

In order to run it you need to:

1. Open Windows PowerShell ISE in Administrator mode. For the better results, our recommendation is to use the advanced connectivity tests which demand to start PowerShell in Administrator mode. You can still run the basic tests, in case you decide not to run this way. Please note that script parameters 'RunAdvancedConnectivityPolicyTests' and 'CollectNetworkTrace' will only work if the admin privileges are granted.

5. Open a New Script window

9. Paste the following in the script window:
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

16. Run it

25. The results can be seen in the output window. If the user has the permissions to create folders, a folder with the resulting log file will be created. When running on Windows, the folder will be opened automatically after the script completes. A zip file with all the log files (AllFiles.zip) will be created. Please send us AllFiles.zip using the 'File upload' option in the 'Details' step.

### More resources

* [Troubleshoot connectivity issues](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database?WT.mc_id=pid:13491:sid:32745425/)
* [SQL Database error codes and corrective actions](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages?WT.mc_id=pid:13491:sid:32745425/)
