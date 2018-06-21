<properties 
	pageTitle="Data factory performance issues" 
	description="My runs are slow, timing out, or delayed" 
	service="microsoft.datafactory" 
    resource="factories"
    authors="arthurw"
    displayOrder="13"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32356642,32356670,32356675"
    productPesIds="15613"
    resourceTags=""
/>

# Data Factory Performance Issues

## **Recommended steps**
- One common reason expected pipeline runs are not happening is that the trigger that is supposed to be starting those runs is either
not started, on the wrong schedule, or missing the expected pipeline reference.  See the pipeline execution and triggers document linked below for details.
- The copy activity performance and tuning guide (document link below) contains detailed information about expected throughput and how to identify and address performance bottlenecks due to a variety of issues with data factory configuration, integration runtime hosting and configuration, underlying data source and sink performance and configuration, serialization/deserialization/compression, and column mapping.
- Review usage of activity policy (properties including retry, timeout, retryIntervalInSeconds) to ensure your activities have appropriate timeouts and aren't stuck in a retry loop with consistent failures.  See the pipelines and activities document linked below for details.
- Review monitoring information for recent in-progress and completed runs.  The easiest way to do that is in the Author and Monitor UI (documentation link below).

## **Recommended documents**
[Pipeline execution and triggers](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers/)<br>
[Copy Activity performance and tuning guide](https://docs.microsoft.com/azure/data-factory/copy-activity-performance/)<br>
[Pipelines and Activities](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities/)<br>
[Monitor Visually](https://docs.microsoft.com/azure/data-factory/monitor-visually/)
