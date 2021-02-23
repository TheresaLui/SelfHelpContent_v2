<properties
  pagetitle="Data Factory Trigger Run&#xD;"
  description="Troubleshoot Azure Data Factory Trigger execution issues."
  service="microsoft.datafactory"
  resource="factories"
  ms.author="kantao"
  selfhelptype="Generic"
  supporttopicids="32749442,32749443,32749444"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="datafactoryrunidtroubleshooter"
  ownershipid="AzureData_DataFactory" />
# Data Factory Trigger Run

## **Recommended Steps**


**Event-based Trigger:** [Create event-based triggers](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger) 
* Make sure that the event trigger is enabled and published. 
* Make sure that the trigger run parameter are used correctly. Supported parameters are @triggerBody().folderPath and @triggerBody().fileName.
* ADF blob events trigger does not guarente the order for event delivery. 
* If the storage account is a Data Lake Storage Gen2 Storage Account and the action is `flush` when the file is uploaded, make sure to have the `close` query parameter as `true`. This setting allows Azure Data Factory to receive notifications when files change. See [Data Lake Storage Gen2 references](https://docs.microsoft.com/rest/api/storageservices/datalakestoragegen2/path/update)

## **Recommended Documents**

* [Pipelines and Activities](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities)
* [Pipeline execution and triggers](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers) 
* [Event-based Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#event-based-trigger) 


### Triggers

* Trigger Pipeline On Demand:

    * [Trigger the pipeline manually](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#trigger-the-pipeline-manually) section under [_Create a pipeline_](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#create-a-pipeline)

* Trigger Pipeline On a Schedule:

    * [Tumbling Window Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger)
    * [Schedule Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger)

* Trigger Pipeline In Response To Events:

    * [Event Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger) for event-driven architecture