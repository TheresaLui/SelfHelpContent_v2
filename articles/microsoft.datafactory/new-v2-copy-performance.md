<properties
	pageTitle="Copy Activity - Understand and Tune Performance"
	description="Guide on understanding and tuning performance of ADF Copy Activity"
	infoBubbleText=""
	service="microsoft.datafactory"
	resource="factories"
	authors="chez-charlie"
	ms.author="chez"
	displayOrder="7"
	articleId="21260b03-9072-4f08-ab96-1aa7398b090e"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32629468"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Understand and Tune Performance of Copy Activity

**Note:** If you use **Self-Hosted IR** please follow the steps on the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** of each IR node, to provide it with the support request.

## **Recommended Steps**

After you run a copy activity, you can collect the run result and performance statistics using the [copy activity monitoring view](https://docs.microsoft.com/azure/data-factory/copy-activity-monitoring), then, you can use the [Troubleshoot copy activity performance](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting) to review:

* Copy Activity [Performance tuning tips and best practices](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting#performance-tuning-tips) including data store specific tips, data store throttling, integration runtime, fault tolerance and staged copy<br>
* Understand [copy activity execution details](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting#understand-copy-activity-execution-details) to help identifying possible bottlenecks you can focus on

Consider using the following guides for tuning and improving the execution of the copy activity:
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
* Please consider creating _activity policy_ (properties including retry, timeout, retryIntervalInSeconds) to ensure your copy activities have appropriate timeouts and won't stuck in a retry loop with consistent failures. For details, see [Pipelines and Activities](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities/) <br>
* See breakdown info of copy stages in _Monitor_ page. For more info, see [Monitor Visually](https://docs.microsoft.com/azure/data-factory/monitor-visually/) <br>
* Benchmark copy performance against recent completed runs in _Monitor_ page. For more info, see [Monitor Visually](https://docs.microsoft.com/azure/data-factory/monitor-visually/) <br>

## **Recommended Documents**

[Copy Activity Performance Troubleshooting](https://docs.microsoft.com/azure/data-factory/copy-activity-performance-troubleshooting)
Copy Activity Performance and Tuning [Guide](https://docs.microsoft.com/azure/data-factory/copy-activity-performance), including following sections: <br>

* [Performance Reference](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#performance-reference) helps you to choose appropriate _DIUs_ and _Self-hosted IR Scalability_ levels <br>
* [Performance Tuning Guidance](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#performance-tuning-steps) <br>
* [Data Integration Units](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#data-integration-units) (DIU, formerly known as Cloud Data Movement Unit or DMU) <br>
* Enable [Parallel Copy](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#parallel-copy) <br>
* Enable [Staged Copy](https://docs.microsoft.com/azure/data-factory/copy-activity-performance#staged-copy) <br>
<br>

