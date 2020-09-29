<properties
	pageTitle="Execute SSIS Package - Data Connectivity Issues"
	description="Troubleshooting Azure-SSIS IR Runtime - Data Connectivity Issues"
	service="microsoft.datafactory"
	resource="factories"
	authors="LianwMS"
	ms.author="lianw"
	articleId="datafactory-newtree-ssis-ir-pacakge-execution-data-connectivity.md"
	displayOrder="12"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32680898"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Execute SSIS Package - Data Connectivity Issues
## **Recommended Steps**

* The ADF Portal can be used to check the output of the SSIS Package Execution Activity including the execution result, error messages, and operation ID. Details can be found at [Monitor the pipeline](https://docs.microsoft.com/azure/data-factory/how-to-invoke-ssis-package-ssis-activity#monitor-the-pipeline).
* The SSIS Catalog (SSISDB) can be used to check the detail logs for the execution. Detail can be found at [Monitor Running Packages and Other Operations](https://docs.microsoft.com/sql/integration-services/performance/monitor-running-packages-and-other-operations?view=sql-server-2017).

**Error message: `"Connection Timeout Expired."` or `"The service has encountered an error processing your request. Please try again."`**

* The Data Source/Destination is overloaded. Check the load on your Data Source/Destination and see whether it has enough capacity. For example, if Azure SQL is used, it's suggested to consider scale up if the Database is likely to time out.
* The network between SSIS Integration Runtime and the Data Source/Destination is unstable, especially when the connection is cross-region or between on-premise and azure. It's suggested to apply retry pattern in SSIS Package by following steps:

	* Make sure your SSIS Packages can rerun on failure without side effects (data loss, data dup...)
	* Configure the **Retry** and **Retry interval** of Execute SSIS Package Activity in the General Tab
	* For ADO.NET and OLEDB Source/Destination component, ConnectRetryCount and ConnectRetryInterval can be set in the Connection Manager in SSIS package or SSIS Activity
	
**Error message: `"ADO NET Source has failed to acquire the connection '...' with the following error message: "A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible."`**

* This issue usually means the Data Source/Destination is inaccessible from SSIS Integration Runtime, which can be caused by different reasons:

	* Make sure you're passing the Data Source/Destination Name/IP correctly
	* Make sure the firewall is set properly
	* Make sure your vNet is configured properly if your Data Source/Destination are in on-premise
	* You can verify whether the issue is from vNet configuration by provisioning an Azure VM in the same vNet, then check whether the Data Source/Destination can be accessed from the Azure VM
	* You can find more details about using vNet with SSIS Integration Runtime at [Join an Azure-SSIS integration runtime to a virtual network](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network)
	
**Error message: "`ADO NET Source has failed to acquire the connection '...' with the following error message: "Could not create a managed connection manager.`"**

* The ADO.NET provider used in the package isn't installed in SSIS Integration Runtime. You can install the provider by using the Custom Setup. More details about Custom Setup can be found in [Customize setup for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-configure-azure-ssis-ir-custom-setup).

**Error message: "`The connection '...' is not found`"**

* This error may be because a known issue in old version SSMS. If the package contains a custom component (For example, SSIS Azure Feature Pack or 3rd party components) which isn't installed on the machine where SSMS is used to do the deployment, the component will be removed by SSMS and cause the error. Upgrade [SSMS](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms) to the latest version that has the issue fixed.<br>

**Error message: "`Microsoft OLE DB Provider for Analysis Services. 'Hresult: 0x80004005 Description:' COM error: COM error: mscorlib; Exception has been thrown by the target of an invocation`"**<br>

* Potential cause & recommended action: One potential cause is that username and password with MFA enabled is configured for Azure Analysis Services authentication, which is not supported in SSIS integration runtime yet. Try to use Service Principal for Azure Analysis Service authentication:<br>
    1. Prepare service principal for AAS [https://docs.microsoft.com/azure/analysis-services/analysis-services-service-principal](https://docs.microsoft.com/azure/analysis-services/analysis-services-service-principal).<br>
    2. In connection manager, configure "Use a specific user name and password": set "AppID" as user name and "clientSecret" as password.<br>

**Error message: "`ADONET Source has failed to acquire the connection {GUID} with the following error message: Login failed for user 'NT AUTHORITY\ANONYMOUS LOGON`" when using managed identity**

* Make sure you don't configure the authentication method of connection manager as "Active Directory Password Authentication" when the parameter "ConnectUsingManagedIdentity" is True. You can configure it as "SQL Authentication" instead which would be ignored if "ConnectUsingManagedIdentity" is set

## **Recommended Documents**

* [Monitor the pipeline](https://docs.microsoft.com/azure/data-factory/how-to-invoke-ssis-package-ssis-activity#monitor-the-pipeline)
* [Monitor Running Packages and Other Operations](https://docs.microsoft.com/sql/integration-services/performance/monitor-running-packages-and-other-operations?view=sql-server-2017)
* [Join an Azure-SSIS integration runtime to a virtual network](https://docs.microsoft.com/azure/data-factory/join-azure-ssis-integration-runtime-virtual-network)
* [Customize setup for the Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/how-to-configure-azure-ssis-ir-custom-setup)
* [Package execution FAQ](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)
