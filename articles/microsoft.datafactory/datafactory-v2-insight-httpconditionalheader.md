<properties
    pageTitle="Copy activity failed due when the condition in Http header is not met"
    description="You use SQL query to pull data from Azure SQL Data Warehouse and hit the following error: 'The condition specified using HTTP conditional header(s) is not met'."
    infoBubbleText="You use SQL query to pull data from Azure SQL Data Warehouse and hit the following error: 'The condition specified using HTTP conditional header(s) is not met'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryHttpConditionalHeaderInsight"
    diagnosticScenario="DataFactoryHttpConditionalHeaderInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due when the condition in Http header is not met'

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures.  One possible cause is that Azure SQL Data Warehouse hit issue querying the external table in Azure Storage.
<!--/issueDescription-->

## **Recommended Steps**

Run the same query in SSMS and check if you see the same result. If yes, open a support ticket to Azure SQL Data Warehouse and provide your SQL DW server and database name to further troubleshoot.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-the-condition-specified-using-http-conditional-headers-is-not-met)
