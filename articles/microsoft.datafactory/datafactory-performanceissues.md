<properties 
	pageTitle="Data factory performance issues" 
	description="My runs are slow, timing out, or delayed" 
	service="microsoft.datafactory" 
    resource="datafactories"
    authors="arthurw"
    displayOrder="12"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32356642,32356670,32356674,32605745"
    productPesIds="15613"
    resourceTags=""
/>

# Data Factory Performance Issues

## **Recommended steps**
- One common scheduling issue that may look like a performance issue is that activities/slices are not running when expected, which is often caused by the activity's input dataset not in Ready state (either because an upstream activity failed or did not run yet, or because the input dataset is external and not ready per validation policy such as the underlying data does not exist or does not meet minimum size constraints, or because the input dataset should be external but does not have the "external" property set to true.
- The copy activity performance and tuning guide (document link below) contains detailed information about expected throughput and how to identify and address performance bottlenecks due to a variety of issues with data factory configuration, integration runtime (Data Management Gateway) hosting and configuration, underlying data source and sink performance and configuration, serialization/deserialization/compression, and column mapping.
- Review usage of activity policy (properties including concurrency, retry, timeout, delay, longRetry, longRetryInterval) to ensure your activities have appropriate timeouts and aren't stuck in a retry loop with consistent failures (Pipelines and activities document link below).

## **Recommended documents**
[Copy Activity performance and tuning guide](https://docs.microsoft.com/azure/data-factory/v1/data-factory-copy-activity-performance/)<br>
[Pipelines and Activities](https://docs.microsoft.com/azure/data-factory/v1/data-factory-create-pipelines/)<br>
[Data Factory Frequently Asked Questions](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq/)
