<properties
  pagetitle="Trigger operations and execution - Unexpected or missing trigger runs "
  service="microsoft.datafactory"
  resource="factories"
  ms.author="spagarwa"
  selfhelptype="Generic"
  supporttopicids="32749447"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="1dfb6b88-8649-4922-b085-0bd2017e72a2"
  ownershipid="AzureData_DataFactory" />
# Trigger operations and execution - Unexpected or missing trigger runs 

## **Recommended Steps**

Resolve common issues related to Azure Data Factory using the following steps.

**Schedule Trigger:** [Create schedule trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger) 

* Make sure that the schedule trigger is enabled and published. 
* Make sure that the created schedule trigger is in the appropriate time zone. Unlike a tumbling window trigger, a schedule trigger supports different time zones.  

**Tumbling Window Trigger:** [Create tumbling window trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger) 

* Make sure that the tumbling window trigger is enabled and published. 
* Make sure that the start time is correct. By design, tumbling window triggers can only be declared in UTC time zone (unlike schedule triggers). 
* The start time of a tumbling window trigger doesn't necessarily indicate the time that the trigger first fires, which may give the impression of missing first runs. The true execution time of the first window is the (start time + interval set) for the trigger. 
* If the number of tumbling window trigger windows is greater than the maximum concurrency set, then it will appear as if there are missing past windows. However, after the execution of the number of current window runs completes, the rest of the trigger runs will be instantiated. 
* Tumbling window triggers represent non-overlapping windows of execution. If a tumbling window trigger is disabled during execution, upon re-enabling, the trigger will backfill and execute new runs from the last completed window. This may create unexpected runs, but this behavior is done by design.  
* Tumbling window triggers may have dependencies that can become stuck, pausing the execution of a run. Make sure to double-check and resolve any dependencies (including self-dependencies) on the trigger.

**Event-based Trigger:** [Create event-based triggers](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger) 

* Make sure that the event trigger is enabled and published. 
* Make sure that the storage account name and container name are correct. 
* If the `blob path begins with` and `blob path ends with` values are specified, make sure they are correct. 
* If the storage account is a Data Lake Storage Gen2 Storage Account and the action is `flush` when the file is uploaded, make sure to have the `close` query parameter as `true`. This setting allows Azure Data Factory to receive notifications when files change. See [Data Lake Storage Gen2 references](https://docs.microsoft.com/rest/api/storageservices/datalakestoragegen2/path/update)

### **Recommended Documents**

* [Pipeline Execution and Triggers](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers)<br>
  See also the following sections: <br>
    * [On-demand Manual Execution](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#manual-execution-on-demand) <br>
    * [Schedule Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#schedule-trigger) triggers pipelines on a wall-clock schedule <br>
    * [Tumbling Window Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#tumbling-window-trigger) fires periodically and retains state <br>
    * [Event-based Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#event-based-trigger) responds to an event in Azure Blob Storage <br>

* Tutorials to create triggers: <br>
    * [Create a Schedule Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger) <br>
    * [Create a Tumbling Window](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger) <br>
    * [Create an Event-based Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger) <br>

* [Tumbling Window Dependency](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency)<br>
   See also the following sections: <br>
    * [Scenarios and Examples](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#usage-scenarios-and-examples) <br>
    * [Create dependency in UI - Screenshot](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#create-a-dependency-in-the-data-factory-ui) <br>
    * [Tumbling Window Dependency Properties](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#tumbling-window-dependency-properties) <br>
    * [Self Dependency](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#tumbling-window-self-dependency-properties) <br>
    * [Monitor Dependencies Experience](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#monitor-dependencies)
