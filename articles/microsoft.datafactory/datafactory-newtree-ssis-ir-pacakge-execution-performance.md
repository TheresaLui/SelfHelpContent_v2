<properties
  pagetitle="Execute SSIS Package - Performance Issues"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="lianw,meiyl"
  selfhelptype="Generic"
  supporttopicids="32680900"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="datafactory-newtree-ssis-ir-pacakge-execution-performance.md"
  ownershipid="AzureData_DataFactory" />
# Execute SSIS Package - Performance Issues

## **Recommended Steps**

### **Scenario 1: If the execution of SSIS activity is stuck or hung**
* Check if the SSIS IR is occupied by other SSIS activities. In the monitoring page of the SSIS IR in ADF portal, you can check the **Concurrent jobs (running/limit)** in the Node detail section. If running jobs has reached the limit, this means that the `maxParallelExecutionsPerNode` is occupied by other SSIS activities. You can increase the node number or `maxParallelExecutionsPerNode`, or cancel the current SSIS activities and try again.
* If your package location is SSIDB, you can first check if the SSISDB has a performance or network issue that caused SSIS IR to fail to pull a task or update a task in SSISDB. We recommend that you increase the SSISDB pricing tier to improve the SSISDB performance.

### **Scenario 2: If the SSIS activity is executed very slowly**
* Check if the SSIS Integration Runtime is in the same region as the Data Source and Destination
* Enable the Performance Logging Level. Set the Logging Level of package execution to **Performance** to collect more information about the duration of each component in the execution. For details, see [Integration Service (SSIS) Logging](https://docs.microsoft.com/sql/integration-services/performance/integration-services-ssis-logging).
* Check IR node performance in the IR monitoring page in Azure portal. Learn how to monitor [Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime#azure-ssis-integration-runtime).
*  The history CPU/memory usage of SSIS Integration Runtime is available in the metrics of the Data Factory in Azure portal.

## **Recommended Documents**

* [Integration Service (SSIS) Logging](https://docs.microsoft.com/sql/integration-services/performance/integration-services-ssis-logging)
* [Azure-SSIS integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime#azure-ssis-integration-runtime)
* [Package execution FAQ](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)
