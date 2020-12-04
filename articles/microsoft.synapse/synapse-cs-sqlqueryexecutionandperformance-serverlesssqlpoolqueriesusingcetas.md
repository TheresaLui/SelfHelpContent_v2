<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783908"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "SQL Query Execution and Performance/Serverless SQL pool - Queries using CETAS"
    description = "SQL Query Execution and Performance/Serverless SQL pool - Queries using CETAS"
    articleId = "synapse-cs-sqlqueryexecutionandperformance-serverlesssqlpoolqueriesusingcetas.md"
    ms.author = "fipopovi, saltug"
/>

# SQL Query Execution and Performance/Serverless SQL pool - Queries using CETAS

## **Recommended Steps**

* Visit [CETAS](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-cetas) for syntax and samples 

* Make sure you are exporting data to supported storage account types as specified in [CETAS in Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-cetas) 

* Make sure you created appropriate credential for both source and destination storage accounts as specified in [control storage access for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control), and have appropriate [permissions](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-cetas#permissions) on destination storage account 

* Make sure you use [data types supported by CETAS](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-cetas#supported-data-types) 

* Make sure destination storage account is in the same region your Serverless SQL pool endpoint is. You can find storage account and workspace regions on Azure Portal, in Overview blades of your storage account and workspace. 

 