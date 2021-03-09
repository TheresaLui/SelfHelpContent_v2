<properties
  pagetitle="V2 Pipeline Errors and Problems&#xD;"
  service=""
  resource=""
  ms.author="pacodel,spagarwa"
  selfhelptype="Generic"
  supporttopicids="32788155"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="31d2e95f-a781-4b9c-98dd-1338efb47e29"
  ownershipid="AzureData_DataFactory" />
# V2 Pipeline Errors and Problems

Resolve most V2 pipeline errors using the following recommendations. 

## **Recommended Steps**

* If each copy activity is taking up to two minutes to start, and the problem occurs primarily on a VNet join (vs. Azure IR), this can be a copy performance issue. Review [Troubleshoot copy activity performance](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting).

* If you encounter a capacity issue from Self-IR, upgrade the VM to increase the node to balance the activities. If you receive an error message about a self-hosted IR general failure or error, a self-hosted IR upgrade, or self-hosted IR connectivity issues--each of which can generate a long queue--see [Troubleshoot self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide).

* If you receive an error message from any source or destination via connectors, which can generate a long queue, see the [Connector Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)

* If you receive an error message about Mapping Data Flow, which can generate a long queue, see the [Data Flows Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide)

* If you receive an error message about other activities, such as Databricks, custom activities, or HDI, which can generate a long queue, see the [Activity Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)

* If you receive an error message about running SSIS packages, which can generate a long queue, see the Azure-SSIS [Package Execution Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq) and [Integration Runtime Management Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot) for more information

* Transient issues can cause activities to be stuck while reporting a new status. We have a background job to recover from this, but it could take up to one hour to run. You can also use timeout and retry policies for activities that support it, and the retry should finish in time. For activities that don't support retry and timeout policies, we recommend that you cancel and rerun the pipeline.

## **Recommended Documents**

1. Troubleshooting Guides:

    * [Troubleshoot self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) 
    * [Activity Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)
    * [Connector Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide) for _Copy_ activities
    * [Data Flows Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-flow-troubleshoot-guide) for _Mapping Data Flow_
    * Azure-SSIS [Package Execution Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-ssis-activity-faq)
    * Azure-SSIS [Integration Runtime Management Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/ssis-integration-runtime-management-troubleshoot)

2. Relevant Concepts:
    * [Pipelines and activities](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities)
    * [Pipeline execution and triggers](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers)

3. How-tos with Sample:
    * [Create pipeline and trigger](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#create-a-pipeline)
    * [Debug and publish the pipeline](https://docs.microsoft.com/azure/data-factory/tutorial-copy-data-portal#debug-and-publish-the-pipeline)

**FAQ**

- [ADF FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
