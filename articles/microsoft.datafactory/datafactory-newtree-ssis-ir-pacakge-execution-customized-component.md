<properties
	pageTitle="Execute SSIS Package - Customized Components Issues"
	description="Troubleshooting Azure-SSIS IR Runtime - Customized Components Issues"
	service="microsoft.datafactory"
	resource="factories"
	authors="LianwMS"
	ms.author="lianw"
	articleId="datafactory-newtree-ssis-ir-pacakge-execution-customized-component.md"
	displayOrder="14"
	selfHelpType="generic"
	supportTopicIds="32680897"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Execute SSIS Package - Customized Components Issues

## **Recommended Steps**

* The ADF Portal can be used to check the output of the SSIS Package Execution Activity including the execution result, error messages, and operation ID. Details can be found at [Monitor the pipeline](https://docs.microsoft.com/azure/data-factory/how-to-invoke-ssis-package-ssis-activity#monitor-the-pipeline).
* The SSIS Catalog (SSISDB) can be used to check the detail logs for the execution. Detail can be found at [Monitor Running Packages and Other Operations](https://docs.microsoft.com/sql/integration-services/performance/monitor-running-packages-and-other-operations?view=sql-server-2017).

**Error message: "`ADO NET Source has failed to acquire the connection '...' with the following error message: "Could not create a managed connection manager.`"**

* The ADO.NET provider used in the package isn't installed in SSIS Integration Runtime. You can install the provider by using the Custom Setup. More details about Custom Setup can be found in [Customize setup for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-configure-azure-ssis-ir-custom-setup)<br>

**Error message: "`The connection '...' is not found`"**

* This error may be because a known issue in old version SSMS. If the package contains a custom component (For example, SSIS Azure Feature Pack or 3rd party components) which isn't installed on the machine where SSMS is used to do the deployment, the component will be removed by SSMS and cause the error. Upgrade [SSMS](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms) to the latest version that has the issue fixed.
* The full FAQ document can be found: [Package execution FAQ](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)

## **Recommended Documents**

* [Monitor the pipeline](https://docs.microsoft.com/azure/data-factory/how-to-invoke-ssis-package-ssis-activity#monitor-the-pipeline)<br>
* [Monitor Running Packages and Other Operations](https://docs.microsoft.com/sql/integration-services/performance/monitor-running-packages-and-other-operations?view=sql-server-2017)<br>
* [Customize setup for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-configure-azure-ssis-ir-custom-setup)<br>
* [Package execution FAQ](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)<br>
