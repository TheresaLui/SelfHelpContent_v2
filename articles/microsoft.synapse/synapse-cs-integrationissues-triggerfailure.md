<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783935"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Integration Issues/Trigger failure"
    description = "Integration Issues/Trigger failure"
    articleId = "synapse-cs-integrationissues-triggerfailure.md"
    ms.author = "saltug"
/>

# Integration Issues/Trigger failure

## **Recommended Steps**

* Pipelines and triggers have a many-to-many relationship:
    * A pipeline can be kicked off by multiple triggers
    * A trigger can kick off multiple pipelines simultaneously

* There are 3 types of triggers available:
    * **Schedule Trigger**: trigger that invokes pipelines on a wall-clock schedule
    * **Tumbling Window trigger**: trigger that operates on a periodic interval, while also retaining state
    * **Event-based trigger**: trigger that responds to an event

* Please be aware of the difference between Schedule and Tumbling Window triggers. See [Trigger Type Comparison](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#trigger-type-comparison) for detailed comparison.

* Please refer to [this document](https://docs.microsoft.com/azure/data-factory/tumbling-window-trigger-dependency?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json) if you want to create dependency for a tumbling window trigger

* Event-based Trigger allows users to ignore _zero-byte blob. For steps to create such trigger, please refer to [Create an Event-based Trigger](https://docs.microsoft.com/azure/data-factory/how-to-create-event-trigger?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json).

## **Recommended Documents**

* [Schedule trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#schedule-trigger)

* [Tumbling window trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#tumbling-window-trigger)

* [Event-based trigger](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#event-based-trigger)

* [Examples of trigger recurrence schedules](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#examples-of-trigger-recurrence-schedules)

* [Trigger type comparison](https://docs.microsoft.com/azure/data-factory/concepts-pipeline-execution-triggers?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#trigger-type-comparison)

 