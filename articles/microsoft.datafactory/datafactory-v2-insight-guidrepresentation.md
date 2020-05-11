<properties
    pageTitle="Copy activity failed due to wrong UUID representation"
    description="Copy data from Azure Cosmos DB and hit error:'The GuidRepresentation for the reader is CSharpLegacy'."
    infoBubbleText="Copy data from Azure Cosmos DB and hit error:'The GuidRepresentation for the reader is CSharpLegacy'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryGuidRepresentationInsight"
    diagnosticScenario="DataFactoryGuidRepresentationInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to wrong UUID representation

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures that may be caused by wrong UUID representation issue.  Please follow the troubleshooting guide below to mitigate
<!--/issueDescription-->

## **Recommended Steps**

In MongoDB connection string, add option "uuidRepresentation=standard".

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-the-guidrepresentation-for-the-reader-is-csharplegacy)
* [MongoDB Connection String](https://docs.microsoft.com/azure/data-factory/connector-mongodb#linked-service-properties)
