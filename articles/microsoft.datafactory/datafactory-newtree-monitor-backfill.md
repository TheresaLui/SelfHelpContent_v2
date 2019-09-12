<properties
    pageTitle="Backfill Data with Tumbling Window Trigger"
    description="Backfill Data with Tumbling Window Trigger"
    infoBubbleText=""
    authors="chez-charlie"
    ms.author="chez"
    articleId="8755ecda-f7be-4a5e-8620-90efd305bd15"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32629503"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public"
/>

# Backfill Data With Azure Data Factory

## **Recommended Steps**

We strongly recommend you to use __Tumbling Window Triggers__ to backfill data, as both _startTime_ and _endTime_ of a tumbling window trigger can be in the past.

**Note:** When there are multiple windows up for execution, especially in a backfill scenario, the order of execution is deterministic, from oldest to newest intervals. Currently, this behavior can't be modified.

## **Recommended Documents**

* [Create a trigger that runs a pipeline on a tumbling window](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger)
* [UI](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger#data-factory-ui) <br>
* [Trigger Type Properties](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger#tumbling-window-trigger-type-properties) <br>
* [Sample](https://docs.microsoft.com/azure/data-factory/how-to-create-tumbling-window-trigger#sample-for-azure-powershell) <br>
