<properties
    pageTitle="Copy activity failed due to unexpected data type decimal(x,x)"
    description="When you copy data from tabular data source (such as SQL Server) into SQL DW using staged copy and PolyBase, you hit the following error: 'Expected data type: DECIMAL(x,x)'."
    infoBubbleText="When you copy data from tabular data source (such as SQL Server) into SQL DW using staged copy and PolyBase, you hit the following error: 'Expected data type: DECIMAL(x,x)'."
    service="microsoft.datafactory"
    resource="factories"
    authors="shelfeng"
    ms.author="shelfeng"
    displayOrder=""
    articleId="DataFactoryExpectedDataTypeInsight"
    diagnosticScenario="DataFactoryExpectedDataTypeInsight"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Copy activity failed due to unexpected data type decimal(x,x)

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Your Data Factory resource <!--$FactoryName-->[FactoryName]<!--/$FactoryName--> has detected run failures that may be caused by the issue that Azure SQL Data Warehouse Polybase cannot insert empty string (null value) into decimal column.  Please follow the troubleshooting guide below to mitigate
<!--/issueDescription-->

## **Recommended Steps**

In Copy activity sink, under Polybase settings, set "use type default" option to false.

## **Recommended Documents**

For more information on this error please follow our troubleshooting doc:

* [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#error-message-expected-data-type-decimalxx-offending-value)
