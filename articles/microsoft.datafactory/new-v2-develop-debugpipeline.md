<properties
  pagetitle="Iterative Development and Debugging Experiences"
  ms.author="chez,vimals"
  selfhelptype="Generic"
  supporttopicids="32629483"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a5f3254f-eb7b-4dd0-a9ee-ffad8c1ff491"
  ownershipid="AzureData_DataFactory" />
# Iterative Development and Debugging Experiences

## **Recommended Steps**

### **Important points to consider**

* We do not support parallelism on debug runs as a design choice. Debug runs are designed to help during authoring and low load testing. You should trigger the pipeline. In case of Dataflow runs, use [*activity runtime*](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging#debugging-a-pipeline-with-a-data-flow-activity) to run activities parallelly. <br>
* We support parallel executions of ForEach iterations for all activities _except_ ExecutePipeline activity
* The Azure Data Factory service only persists debug run history for 15 days

## **Recommended Documents**

* [Debugging a pipeline](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging#debugging-a-pipeline)
* [Monitor debug runs](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging#monitoring-debug-runs) <br>
* [Debug mapping dataflows](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging#debugging-mapping-data-flows) <br>
* [Set breakpoints for debugging](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging#setting-breakpoints) <br>
