<properties
    pageTitle="Copy activity failed due to error 403 (Forbidden)"
    description="Your copy activity failed with error 403 (Forbidden)."
    infoBubbleText="Your copy activity failed with error 403 (Forbidden)."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryServerErrorForbiddenInsight"
    diagnosticScenario="DataFactoryServerErrorForbiddenInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to error 403 (Forbidden)'

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures.  One possible cause is that the service principal or managed identity you use doesn't have permission to access the certain folder/file.
<!--/issueDescription-->

## **Recommended Steps**

Grant corresponding permissions on all the folders and subfolders you need to copy.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage)
