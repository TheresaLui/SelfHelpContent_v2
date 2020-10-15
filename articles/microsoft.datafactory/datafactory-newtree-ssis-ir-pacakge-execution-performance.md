<properties
	pageTitle="Execute SSIS Package - Performance Issues"
	description="Troubleshooting Azure-SSIS IR Runtime - Performance Issues"
	service="microsoft.datafactory"
	resource="factories"
	authors="LianwMS"
	ms.author="lianw"
	articleId="datafactory-newtree-ssis-ir-pacakge-execution-performance.md"
	displayOrder="15"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32680900"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Execute SSIS Package - Performance Issues
## **Recommended Steps**

* Check if the SSIS Integration Runtime is in the same region as the Data Source and Destination
* Enable "Performance" Logging Level. You can set the Logging Level of package execution to "Performance" to collect more detail duration information for each component in the execution. Details can be found at: [Integration Service (SSIS) Logging](https://docs.microsoft.com/sql/integration-services/performance/integration-services-ssis-logging)
* Check IR node performance in IR monitor page in Azure portal. How to monitor SSIS Integration Runtime: [Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime#azure-ssis-integration-runtime)
*  The history CPU/Memory usage of SSIS Integration Runtime is available at the Metrics of the Data Factory in Azure portal<br>

## **Recommended Documents**

* [Integration Service (SSIS) Logging](https://docs.microsoft.com/sql/integration-services/performance/integration-services-ssis-logging)
* [Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime#azure-ssis-integration-runtime)
* [Package execution FAQ](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)
