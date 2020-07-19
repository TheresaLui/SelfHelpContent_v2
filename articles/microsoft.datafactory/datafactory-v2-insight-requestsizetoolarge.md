<properties
    pageTitle="Copy activity failed due to request size too large"
    description="Copy data into Azure Cosmos DB with default write batch size, and hit error 'Request size is too large'."
    infoBubbleText="Copy data into Azure Cosmos DB with default write batch size, and hit error 'Request size is too large'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryRequestSizeTooLargeInsight"
    diagnosticScenario="DataFactoryRequestSizeTooLargeInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to request size too large

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures.  One possible cause is that the request size too large.  Please follow the troubleshooting guide below to mitigate
<!--/issueDescription-->

## **Recommended Steps**

Solution 1: Increase the container RU to bigger value in Cosmos DB, which will improve the copy activity performance, though incur more cost in Cosmos DB.

Solution 2: Decrease writeBatchSize to smaller value (such as 1000) and set parallelCopies to smaller value such as 1, which will make copy run performance worse than current but will not incur more cost in Cosmos DB.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-request-size-is-too-large)
