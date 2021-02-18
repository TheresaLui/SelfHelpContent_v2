<properties
    pageTitle="Data Factory Pipeline Stuck in Queued"
    description="Data Factory Pipeline Stuck in Queued"
    infoBubbleText="Data Factory Pipeline Stuck in Queued"
    service="microsoft.datafactory"
    resource="factories"
    authors="grorcai"
    ms.author="grorcai-msft"
    displayOrder="1"
    articleId="462949d1-76b7-4c18-ae04-2b1d6c64c541"
    diagnosticScenario="DataFactoryPipelineQueuedInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32680901,32629491"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, BlackForest, Fairfax, Mooncake, usnat, ussec"
	  ownershipId="AzureData_DataFactory"
/>

# Pipeline Stuck in Queued Insight 

## We ran diagnostics on your resource and found the following

<!--issueDescription-->
Based on the Run ID provided, we see that there are other runs in `InProgress` status at the same time for the Pipeline <!--$pipelineName-->[pipelineName]<!--/$pipelineName-->. The reason for the long Queued status might be due to Pipeline concurrency setting.
<!--/issueDescription-->

## **Recommended Steps**

Check the concurrency setting in Pipeline <!--$pipelineName-->[pipelineName]<!--/$pipelineName-->. Remove the concurrency value or set the concurrency value to a larger number.
