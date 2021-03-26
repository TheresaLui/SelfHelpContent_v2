<properties
  pagetitle="V2 Pipeline Activity Errors and Problems"
  service=""
  resource=""
  ms.author="pacodel,spagarwa,susabat"
  selfhelptype="Generic"
  supporttopicids="32788532"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="31d2e95f-a781-4b9c-98dd-1338efb47e29"
  ownershipid="AzureData_DataFactory" />
# V2 Pipeline Activity Errors and Problems

You can resolve most V2 pipeline activity errors and issues by using the following recommendations. 

## **Recommended Steps**
### Longer than normal copy start times
* If each copy activity is taking up to two minutes to start, and the issue occurs primarily on a VNet join (vs. Azure IR), this can be a copy performance issue. To review troubleshooting steps, see [Troubleshoot copy activity performance](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting).

### Increase Data Flow activity start up time
* You can use a TTL (time-to-live) option in the Azure Integration Runtime for Data Flow properties to reduce data flow activity times. For details, see [Data Flow intergation runtime setup ](https://docs.microsoft.com/azure/data-factory/control-flow-execute-data-flow-activity#data-flow-integration-runtime).

### Encountering capacity issues
* If you encounter a capacity issue from Self-IR, upgrade the VM to increase the node to balance the activities. If you receive an error message about a self-hosted IR general failure or error, a self-hosted IR upgrade, or self-hosted IR connectivity issues, which can generate a long queue, see [Troubleshoot self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide).

### Displaying error messages 
* If you receive an error message from any source or destination via connectors, which also can generate a long queue, see the [Connector Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)

* If you receive an error message about Mapping Data Flow, which also can generate a long queue, see the [Data Flows Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide)

* If you receive an error message about other activities that can generate a long queue, such as Databricks, custom activities, or HDI, see the [Activity Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)

* If you receive an error message about running SSIS packages, which can generate a long queue, see the Azure-SSIS [Package Execution Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq) and the [Integration Runtime Management Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot)

* Transient issues can cause activities to be stuck while reporting a new status. You may see Internal Server Error message. You have a background job to recover from this, but it could take up to one hour to run or can display 500 error code. You can use timeout and retry policies for activities that support it, and the retry should finish in time. For activities that don't support retry and timeout policies, we recommend that you cancel and rerun the pipeline.

## **Recommended Documents**

Troubleshooting guides:

 * [Troubleshoot self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) 
 * [Activity Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)
 * [Connector Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide) for _Copy_ activities
 * [Data Flows Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide) for _Mapping Data Flow_
 * Azure-SSIS [Package Execution Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)
 * Azure-SSIS [Integration Runtime Management Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot)
 * [Pipeline and trigger Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/pipeline-trigger-troubleshoot-guide)

Relevant concepts:
 * [Pipelines and activities](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities)
 * [Pipeline execution and triggers](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers)
 * [Monitor Data Flow Actvity](https://docs.microsoft.com/azure/data-factory/control-flow-execute-data-flow-activity#monitoring-the-data-flow-activity) 

How-tos with samples:
 * [Create pipeline and trigger](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#create-a-pipeline)
 * [Debug and publish the pipeline](https://docs.microsoft.com/azure/data-factory/tutorial-copy-data-portal#debug-and-publish-the-pipeline)

**FAQ**
- [ADF FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
