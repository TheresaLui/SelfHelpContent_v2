<properties
	pageTitle="Azure-SSIS IR General start and stop Issues"
	description="Troubleshooting Azure-SSIS IR Management - General start and stop Issues"
	service="microsoft.datafactory"
	resource="factories"
	authors="chinadragon0515"
	ms.author="dashe"
	articleId="datafactory-newtree-ssis-ir-management-general-start-stop.md"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32680895"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Azure-SSIS IR General start and stop Issues

The ADF Portal can be used to check the result of Azure SSIS IR start and there is detail error message shows on the ADF portal. The start result can also be retrieved via Azure powershell command.

## **Recommended Steps**

* Get the error code in the error message and then search the [troubleshoot document](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot) of the error code and find the detail cause and solution

### Common errors, causes, and solutions

The common error will be Azure SQL Server or Managed Instance related.

An Azure SQL Database server or managed instance is required if you're provisioning SSIS IR with an SSIS catalog database. The SSIS IR must be able to access the Azure SQL Database server or managed instance. Also, the account of the Azure SQL Database server or managed instance should have permission to create an SSIS catalog database (SSISDB). If there's an error, an error code with a detailed SQL exception message will be shown in the Data Factory portal. Use the information in the following list to troubleshoot the error codes.

### AzureSqlConnectionFailure

You might see this issue when you're provisioning a new SSIS IR or while IR is running. If you experience this error during IR provisioning, you might get a detailed SqlException message in the error message that indicates one of the following problems:

* A network connection issue. Check whether the SQL Server or managed instance hostname is accessible. Also verify that no firewall or network security group (NSG) is blocking SSIS IR access to the server.
* Login failed during SQL authentication. The account provided can't sign in to the SQL Server database. Make sure you provide the correct user account.
* Login failed during Microsoft Azure Active Directory (Azure AD) authentication (managed identity). Add the managed identity of your factory to an AAD group, and make sure the managed identity has access permissions to your catalog database server.
* Connection timeout. This error is always caused by a security-related configuration. We recommend that you:

  1. Create a new VM
  2. Join the VM to the same Microsoft Azure Virtual Network of IR if IR is in a virtual network
  3. Install SSMS and check the Azure SQL Database server or managed instance status

For other problems, fix the issue shown in the detailed SQL Exception error message. If you’re still having problems, contact the Azure SQL Database server or managed instance support team.

If you see the error when IR is running, network security group or firewall changes are likely preventing the SSIS IR worker node from accessing the Azure SQL Database server or managed instance. Unblock the SSIS IR worker node so that it can access the Azure SQL Database server or managed instance.

### CatalogCapacityLimitError

Here's what this kind of error message might look like: "The database 'SSISDB' has reached its size quota. Partition or delete data, drop indexes, or consult the documentation for possible resolutions."

The possible solutions are:

* Increase the quota size of your SSISDB
* Change the configuration of SSISDB to reduce the size by:

   * Reducing the retention period and number of project versions
   * Reducing the retention period of the log
   * Changing the default level of the log

### CatalogDbBelongsToAnotherIR

This error means the Azure SQL Database server or managed instance already has an SSISDB and that it's being used by another IR. You need to either provide a different Azure SQL Database server or managed instance or else delete the existing SSISDB and restart the new IR.

### CatalogDbCreationFailure

This error can occur for one of the following reasons:

* The user account that's configured for the SSIS IR doesn't have permission to create the database. You can grant the user permission to create the database.
* A timeout occurs during database creation, such as an execution timeout or a DB operation timeout. You should retry the operation later. If the retry doesn’t work, contact the Azure SQL Database server or Managed Instance support team.

For other issues, check the SQL Exception error message and fix the issue mentioned in the error details. If you’re still having problems, contact the Azure SQL Database server or managed instance support team.

### InvalidCatalogDb

This kind of error message looks like this: "Invalid object name 'catalog.catalog_properties'." In this situation, either you already have a database named SSISDB but it wasn't created by SSIS IR, or the database is in an invalid state that's caused by errors in the last SSIS IR provisioning. You can drop the existing database with the name SSISDB, or you can configure a new Azure SQL Database server or managed instance for the IR.

## **Recommended Documents**

* [Create Azure-SSIS Integration Runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/create-azure-ssis-integration-runtime)
* [Enable Azure Active Directory authentication for Azure-SSIS Integration Runtime](https://docs.microsoft.com/azure/data-factory/enable-aad-authentication-azure-ssis-ir)
* [Manage an integration runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/manage-azure-ssis-integration-runtime)
* [Monitor an integration runtime in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime#azure-ssis-integration-runtime)
* [How to start and stop Azure-SSIS Integration Runtime on a schedule](https://docs.microsoft.com/azure/data-factory/how-to-schedule-azure-ssis-integration-runtime)
