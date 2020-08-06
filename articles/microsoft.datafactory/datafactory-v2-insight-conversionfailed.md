<properties
    pageTitle="Copy activity failed due to conversion error"
    description="Copy data from tabular data source to Azure Data Warehouse using polybase and hit error:'Conversion failed when converting from a character string to uniqueidentifier'."
    infoBubbleText="Copy data from tabular data source to Azure Data Warehouse using polybase and hit error:'Conversion failed when converting from a character string to uniqueidentifier'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryConversionFailedInsight"
    diagnosticScenario="DataFactoryConversionFailedInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to conversion error

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures that may be caused by the issue that PolyBase cannot convert empty string to GUID.  Please follow the troubleshooting guide below to mitigate
<!--/issueDescription-->

## **Recommended Steps**

In Copy activity sink, under Polybase settings, set "use type default" option to false.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-conversion-failed-when-converting-from-a-character-string-to-uniqueidentifier)
