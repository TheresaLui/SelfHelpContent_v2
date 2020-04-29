<properties
    pageTitle="Data Factory Trigger Information"
    description="Data Factory Trigger Information"
    infoBubbleText="Data Factory Trigger Information"
    service="microsoft.datafactory"
    resource="factories"
    authors="grorcai"
    ms.author="grorcai"
    displayOrder="1"
    articleId="DataFactoryTriggerInfoInsight"
    diagnosticScenario="DataFactoryTriggerInfoInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, BlackForest, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Run specific status of the trigger

Based on the Run ID provided we can see it was triggered by <!--$triggerName-->[triggerName]<!--/$triggerName-->, which was <!--$runTimeState-->[runTimeState]<!--/$runTimeState--> at the run time.

Based on the Run ID provided we can see it was wrongly triggered by trigger12, which was Activated at the run time.<BR><BR>It is a TumblingWindowTrigger and this trigger run was for the following window:<BR> <BR>Window Start: 2020-04-22T02:51:00<BR> Window End: 2020-04-22T03:06:00

## **Recommended Steps**

*  Please, double check if the Trigger was Activated at the runtime and which was the reason for the Trigger had started.
