<properties
  pagetitle="Understand and Tune Performance of Copy Activity"
  description="Guide on understanding and tuning performance of ADF Copy Activity"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,brianwan"
  selfhelptype="Generic"
  supporttopicids="32629468"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="21260b03-9072-4f08-ab96-1aa7398b090e"
  ownershipid="AzureData_DataFactory" />
# Understand and Tune Performance of Copy Activity

Troubleshoot and tune performance of copy activity using these resources. 

## Troubleshooting performance issue

When troubleshooting performance issues, refer to the copy status to better understand time spent from the source or destination.
* If the greatest amount of time was spent from the source, focus on the source from IR. This can point to either a source side issue or a connectivity issue between the IR and Source. For details, refer to [Performance troubleshooting](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting).
* If you want to focus on the network between the IR and Source/Sink, check for any retransmission between the Integration Runtime and the Source/Sink.

**Note:** If you use Self-Hosted IR, follow the steps in this [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory). Make sure to note the **Report ID** of each IR node to provide it with the support request.

## **Recommended Steps**

After you run a copy activity, collect the run result and performance statistics using the [copy activity monitoring view](https://docs.microsoft.com/azure/data-factory/copy-activity-monitoring), then, you can use the [Troubleshoot copy activity performance](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting) to review:

* Copy Activity [Performance tuning tips and best practices](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting#performance-tuning-tips) including data store specific tips, data store throttling, integration runtime, fault tolerance and staged copy<br>
* Understand [copy activity execution details](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting#understand-copy-activity-execution-details) to help identifying possible bottlenecks

Consider the following guides for tuning and improving the execution of the copy activity:
* [Copy Activity performance features](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-features) outlines the copy activity performance optimization features that you can leverage in Azure Data Factory, including:
  * [Data Integration Units](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-features#data-integration-units) when using Azure IR <br>
  * Self-hosted IR [Scalability](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-features#self-hosted-integration-runtime-scalability)
  * [Parallel Copy](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-features#parallel-copy) which applies for both, Azure IR and Self-hosted IR scenarios <br>

* [Performance Tuning Guide](https://docs.microsoft.com/azure/data-factory/copy-activity-performance) offers detailed information about expected throughput and how to identify and address performance bottlenecks due to a variety of issues, including: <br>
  * Data factory configuration <br>
  * Integration runtime hosting and configuration <br>
  * Underlying data source and sink performance and configuration <br>
  * Serialization/deserialization/compression <br>
  * Column mapping <br>
* Consider creating _activity policy_ (properties including retry, timeout, retryIntervalInSeconds) to ensure your copy activities have appropriate timeouts and won't get stuck in a retry loop with consistent failures. For details, see [Pipelines and Activities](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities/) <br>
* See breakdown info of copy stages in _Monitor_ page. For more info, see [Monitor Visually](https://docs.microsoft.com/azure/data-factory/monitor-visually/) <br>
* Benchmark copy performance against recent completed runs in _Monitor_ page. For more info, see [Monitor Visually](https://docs.microsoft.com/azure/data-factory/monitor-visually/) <br>


## How to write high performance custom ADF Copy code

Most users are able to resolve issues regarding custom ADF copy code performance and intermittent errors by using the steps below.

* Instead of `client.Factories.List()`, use  `client.Factories.Get()` by `dataFactoryName`.<br>

* Use `GET` with the Data Factory Name to reduce the number of list factories objects that are called.<br>

* Use the [SQL Server Bulk Copy](https://docs.microsoft.comdotnet/framework/data/adonet/sql/bulk-copy-operations-in-sql-server) method..<br>

* [ADF Copy SDK](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-dot-net) .<br>

## **Recommended Documents**

* [Copy Activity Performance Troubleshooting](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting)
* Copy Activity Performance and Tuning [Guide](https://docs.microsoft.com/azure/data-factory/copy-activity-performance), including following sections: <br>
	
	* [Performance Reference](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#performance-reference) helps you to choose appropriate _DIUs_ and _Self-hosted IR Scalability_ levels <br>
	* [Performance Tuning Guidance](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#performance-tuning-steps) <br>
	* [Data Integration Units](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#data-integration-units) (DIU, formerly known as Cloud Data Movement Unit or DMU) <br>
	* Enable [Parallel Copy](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#parallel-copy) <br>
	* Enable [Staged Copy](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#staged-copy) <br>
