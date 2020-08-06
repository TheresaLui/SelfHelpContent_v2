<properties
    pageTitle="V2 - Pipeline Error or Trigger Failure - Missing Trigger Runs and Pipeline Runs Common Solutions"
    description="V2 - Pipeline Error or Trigger Failure - Missing Trigger Runs and Pipeline Runs Common Solutions"
    service=""
    resource=""
    authors="chez-charlie"
    ms.author="chez"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637151, 32680902, 32680903"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1dfb6b88-8649-4922-b085-0bd2017e72a2"
	ownershipId="AzureData_DataFactory"
/>

# V2 - Triggers

## **Recommended Steps**

1. Pipelines and triggers have a _many-to-many_ relationship:

    * A pipeline can be kicked off by multiple triggers
    * A trigger can kick off multiple pipelines simultaneously

1. There are 3 types of triggers available in Azure Data Factory:

    * Schedule Trigger: trigger that invokes pipelines on a wall-clock schedule
    * Tumbling Window trigger: trigger that operates on a periodic interval, while also _retaining state_
    * Event-based trigger: trigger that responds to an event

1. Please be aware of the difference between _Schedule_ and _Tumbling Window_ triggers. See [Trigger Type Comparison](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#trigger-type-comparison) for detailed comparison.
1. Please refer to this [document](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency) if you want to create dependency for a tumbling window trigger 
1. Event-based Trigger allows users to ignore _zero-byte blob. For steps to create such trigger, please refer to [Create an Event-based Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger).

## **Recommended Documents**

1. Pipeline Execution and Triggers [Document](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers), including following sections: <br>
    * [On-demand Manual Execution](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#manual-execution-on-demand) <br>
    * [Schedule Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#schedule-trigger) triggers pipelines on a wall-clock schedule <br>
    * [Tumbling Window Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#tumbling-window-trigger) fires periodically and retains state <br>
    * [Event-based Trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#event-based-trigger) responds to an event in Azure Blob Storage <br>
    * __Please read__ Schedule Trigger versus Tumbling Window Trigger [Comparison](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers#trigger-type-comparison) <br>

1. Create Triggers: <br>
    * Create a Schedule Trigger [Tutorial](https://docs.microsoft.com/azure/data-factory/how-to-create-schedule-trigger) <br>
    * Create a Tumbling Window [Tutorial](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger) <br>
    * Create an Event-based Trigger [Tutorial](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger) <br>

1. Tumbling Window Dependency [Document](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency), including following sections: <br>
    * [Scenarios and Examples](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#usage-scenarios-and-examples) <br>
    * Create dependency in UI [Screenshot](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#create-a-dependency-in-the-data-factory-ui) <br>
    * Tumbling Window Dependency [Properties](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#tumbling-window-dependency-properties) <br>
    * Self Dependency [Properties](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#tumbling-window-self-dependency-properties) <br>
    * Monitor Dependencies [Experience](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency#monitor-dependencies)
