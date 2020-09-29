<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SQLDataWarehouse"
    service = "microsoft.synapse"
    resource = ""
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32743060"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "SQL Performance and Query Execution/SQL pool queries using PREDICT"
    description = "SQL Performance and Query Execution/SQL pool queries using PREDICT"
    articleId = "synapse-sqlperformanceandqueryexecution-sqlpoolqueriesusingpredict.md"
    authors = "saltug"
    ms.author = "saltug"
/>

# SQL Performance and Query Execution/SQL pool queries using PREDICT

## **Recommended Steps**
* T-SQL Predict is used for batch scoring scenario in the data warehouse without moving the data out of the data warehouse. See [documentation](https://docs.microsoft.com/sql/t-sql/queries/predict-transact-sql) for details.
* Only models of ONNX format are supported with the Predict statement in the data warehouse.
* The column names of the scoring input data should match the column names of the model inputs.
* Data warehouse doesn't support multidimensional array so ensure that the training inputs are individual inputs instead of an array.

## **Recommended Documents**
* [PREDICT (Transact-SQL)](https://docs.microsoft.com/sql/t-sql/queries/predict-transact-sql)