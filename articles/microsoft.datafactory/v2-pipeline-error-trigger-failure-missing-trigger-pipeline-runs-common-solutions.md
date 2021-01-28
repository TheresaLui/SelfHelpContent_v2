<properties
  pagetitle="V2 - Triggers&#xD;"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,vimals"
  selfhelptype="Generic"
  supporttopicids="32749447"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="1dfb6b88-8649-4922-b085-0bd2017e72a2"
  ownershipid="AzureData_DataFactory" />
# V2 - Triggers

Resolve common issues related to Azure Data Factory triggers v2 using the following steps.

## **Recommended Steps**

1. Pipelines and triggers have a _many-to-many_ relationship:
    * A pipeline can be kicked off by multiple triggers
    * A trigger can kick off multiple pipelines simultaneously

1. There are 3 types of triggers available in Azure Data Factory:
    * Schedule Trigger: It invokes pipelines on a clock-based schedule
    * Tumbling Window trigger: It operates on a periodic interval, while also _retaining state_
    * Event-based trigger: It responds to an event

1. Note the difference between _Schedule_ and _Tumbling Window_ triggers. See [Trigger Type Comparison](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#trigger-type-comparison) for detailed comparison.
1. To create dependency for a tumbling window trigger, refer to this [document](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency) 
1. Event-based Trigger allows users to ignore _zero-byte blob_. For steps to create such a trigger, refer to the tutorials in the next section.

## **Recommended Documents**

* Pipeline Execution and Triggers [Document](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers)<br>
  See also the following sections: <br>
    * [On-demand Manual Execution](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#manual-execution-on-demand) <br>
    * [Schedule Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#schedule-trigger) triggers pipelines on a wall-clock schedule <br>
    * [Tumbling Window Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#tumbling-window-trigger) fires periodically and retains state <br>
    * [Event-based Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#event-based-trigger) responds to an event in Azure Blob Storage <br>

* Tutorials to create Triggers: <br>
    * Create a Schedule Trigger [Tutorial](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger) <br>
    * Create a Tumbling Window [Tutorial](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger) <br>
    * Create an Event-based Trigger [Tutorial](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger) <br>

* [Tumbling Window Dependency](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency)<br>
   See also the following sections: <br>
    * [Scenarios and Examples](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#usage-scenarios-and-examples) <br>
    * Create dependency in UI [Screenshot](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#create-a-dependency-in-the-data-factory-ui) <br>
    * Tumbling Window Dependency [Properties](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#tumbling-window-dependency-properties) <br>
    * Self Dependency [Properties](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#tumbling-window-self-dependency-properties) <br>
    * Monitor Dependencies [Experience](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#monitor-dependencies)
