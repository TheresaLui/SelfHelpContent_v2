<properties
    pageTitle="Copy activity failed due to request rate is large"
    description="Copy data into Azure Cosmos DB with default write batch size, and hit error 'Request rate is large'."
    infoBubbleText="Copy data into Azure Cosmos DB with default write batch size, and hit error 'Request rate is large'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryRequestRateIsLargeInsight"
    diagnosticScenario="DataFactoryRequestRateIsLargeInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to request rate is large

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures.  One possible cause is that the request rate is large.  Please follow the troubleshooting guide below to mitigate
<!--/issueDescription-->

## **Recommended Steps**

In copy activity sink, reduce the 'Write batch size' value (default value is 10000).

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-request-rate-is-large)
