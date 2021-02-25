<properties
  pagetitle="Pipeline Concurrency"
  description="Pipeline Concurrency or Degree of Parallelism Common Solutions"
  service=""
  resource=""
  ms.author="jaserano,lijzha"
  selfhelptype="Generic"
  supporttopicids="32680901"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="1a1d9928-f072-4e3c-ba3f-a5591ecfedf5"
  ownershipid="AzureData_DataFactory" />
# Pipeline Concurrency

Resolve common issues with pipeline concurrency by reviewing these steps.

## **Recommended Steps**

### Pipeline concurrency limit

The concurrency config in pipeline represents the maximum number of concurrent runs, range of the config: 1-50. If the concurrency limit is reached, additional pipeline runs are queued until earlier ones complete. Maximum number of queued runs: 100.

### Can I request to increase the concurrency to exceed 50?

No, 50 is the maximum when concurrency is set.

### What's the default concurrency when the config is not set?

By default, it's unlimited.

### How to allow multiple concurrent runs for a pipeline but limit the concurrency for some scenarios?

If a pipeline is well parameterized and designed to be used for multiple scenarios based on input, it's possible that the pipeline can run concurrently without limit while some scenarios need to be limited. In this case, consider use tumbling window trigger with concurrency based on requirement, and leave pipeline concurrency unset. Multiple triggers can be configured to trigger same pipeline with different inputs to serve different scenarios.

## **Recommended Documents**

- [Pipelines and Activities](https://docs.microsoft.com/en-us/azure/data-factory/concepts-pipelines-activities#pipeline-json)
- [Data Factory Limits](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#data-factory-limits)