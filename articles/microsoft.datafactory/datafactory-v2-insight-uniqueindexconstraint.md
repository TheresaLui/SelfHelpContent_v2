<properties
    pageTitle="Copy activity failed due to unique index constraint violation"
    description="Copy data into Azure Cosmos DB and hit error 'Unique index constraint violation'."
    infoBubbleText="Copy data into Azure Cosmos DB and hit error 'Unique index constraint violation'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryUniqueIndexConstraintInsight"
    diagnosticScenario="DataFactoryUniqueIndexConstraintInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to unique index constraint violation

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures that may be caused by unique index constraint violation issue.  Please follow the troubleshooting guide below to mitigate
<!--/issueDescription-->

## **Recommended Steps**

If you use Insert as write behavior, set Upsert as write behavior.
If you use Upsert as write behavior and you set another unique key to the container, make sure each document has different value for defined unique key.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-unique-index-constraint-violation)
