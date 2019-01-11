<properties
    pageTitle="Copy Activity - Fault Tolerance and Error Handling"
    description="Fault tolerance of copy activity in Azure Data Factory"
    infoBubbleText=""
    authors="chez-charlie"
    ms.author="chez"
    articleId=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32629465"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public"
/>

# Fault Tolerance and Error Handling for Copy Activity in Azure Data Factory

## **Recommended Steps**

To change the default behavior, which fails the copy activity when incompatible data is encountered, you can choose to add tolerance and skip incompatible data row. <br>
List of supported scenarios include: <br>

* Incompatibility between the source data type and the sink native type <br>
* Mismatch in the number of columns between the source and the sink <br>
* Primary key violation when writing to SQL Server/Azure SQL Database/Azure Cosmos DB <br>

## **Recommended Documents**

Fault Tolerance and Error Handling [Documentation](https://docs.microsoft.com/azure/data-factory/copy-activity-fault-tolerance) <br>

* [Supported Scenarios](https://docs.microsoft.com/azure/data-factory/copy-activity-fault-tolerance#supported-scenarios) <br>
* [Configuration](https://docs.microsoft.com/azure/data-factory/copy-activity-fault-tolerance#configuration) <br>
* [Monitor Skipped Rows](https://docs.microsoft.com/azure/data-factory/copy-activity-fault-tolerance#monitor-skipped-rows) <br>
