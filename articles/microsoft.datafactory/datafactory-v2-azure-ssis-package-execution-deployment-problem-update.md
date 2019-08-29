<properties
    pageTitle="V2 - Azure-SSIS/Package Execution or Deployment Problem Common Solutions Update"
    description="V2 - Azure-SSIS/Package Execution or Deployment Problem Common Solutions Update"
    service=""
    resource=""
    authors="v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629548"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public"
    articleId="7c16030e-6550-4e50-9e61-99a3f1ae2871"
/>

# V2 - Azure-SSIS/Package Execution or Deployment Problem Common Solutions Update

## **Recommended Steps**

**Error message: "ADO NET Source has failed to acquire the connection '...' " with "A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible."**

This issue usually means the data source or destination is inaccessible from the SSIS integration runtime. The reasons can vary.

Try these actions:

* Verify that you're passing the data source or destination name/IP correctly<br>
* Verify that the firewall is set properly<br>
* Verify that your virtual network is configured properly if your data source or destination is on-premises:
  
  * You can verify whether the issue is from virtual network configuration by provisioning an Azure VM in the same virtual network, then check whether the data source or destination can be accessed from the Azure VM
  * You can find more details about using a virtual network with an SSIS integration runtime in [Join an Azure-SSIS integration runtime to a virtual network](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network)

**Error message: "The connection '...' is not found"**

A known issue in older versions of SQL Server Management Studio (SSMS) can cause this error. If the package contains a custom component (for example, SSIS Azure Feature Pack or partner components) that isn't installed on the machine where SSMS is used to do the deployment, SSMS will remove the component and cause the error. Upgrade SSMS to the latest version that has the issue fixed.

**Error message: "The database 'SSISDB' has reached its size quota"**

A potential cause is that the SSISDB database created in the Azure SQL database, or a managed instance when you're creating an SSIS integration runtime, has reached its quota.

Try these actions:

* Consider increasing the DTU of your database. You can find details in [SQL Database resource limits for an Azure SQL Database server](https://docs.microsoft.com/azure/sql-database/sql-database-resource-limits-database-server).<br>
* Check whether your package would generate many logs. If so, you can configure an elastic job to clean up these logs. For details, see [Clean up SSISDB logs with Azure Elastic Database jobs](https://docs.microsoft.com/azure/data-factory/how-to-clean-up-ssisdb-logs-with-elastic-jobs).

For more information on additional common errors and solutions please review our [Troubleshooting documentation](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq).

## **Recommended Documents**

### Package Execution

* [Run an SSIS package with the Execute SSIS Package activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/how-to-invoke-ssis-package-ssis-activity)<br>
* [Install paid or licensed custom components. Third Party Component for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-develop-azure-ssis-ir-licensed-components)

### FAQ

* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)<br>
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
