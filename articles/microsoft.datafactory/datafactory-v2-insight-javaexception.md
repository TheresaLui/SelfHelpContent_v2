<properties
    pageTitle="Copy activity failed due to Java error"
    description="You copy data into Azure SQL Data Warehouse using PolyBase, and hit Java exception 'HdfsBridge::CreateRecordReader'."
    infoBubbleText="You copy data into Azure SQL Data Warehouse using PolyBase, and hit Java exception 'HdfsBridge::CreateRecordReader'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryJavaExceptionInsight"
    diagnosticScenario="DataFactoryJavaExceptionInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to Java exception 'HdfsBridge::CreateRecordReader'

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures.  One possible cause is that the schema (total column width) being too large (larger than 1 MB).
<!--/issueDescription-->

## **Recommended Steps**

Please reduce column width to be less than 1 MB.  Or use bulk insert approach by disabling Polybase.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-java-exception-messagehdfsbridgecreaterecordreader)
