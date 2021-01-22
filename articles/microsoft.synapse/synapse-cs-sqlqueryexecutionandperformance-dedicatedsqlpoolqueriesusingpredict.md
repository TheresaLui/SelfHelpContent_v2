<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783867"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "SQL Query Execution and Performance/Dedicated SQL pool - Queries using PREDICT"
    description = "SQL Query Execution and Performance/Dedicated SQL pool - Queries using PREDICT"
    articleId = "synapse-cs-sqlqueryexecutionandperformance-dedicatedsqlpoolqueriesusingpredict.md"
    ms.author = "saltug"
/>

# SQL Query Execution and Performance/Dedicated SQL pool - Queries using PREDICT

## **Recommended Steps**

* T-SQL Predict is used for batch scoring scenario in the Dedicated SQL pool without moving the data out of the Dedicated SQL pool. See [documentation](https://docs.microsoft.com/sql/t-sql/queries/predict-transact-sql) for details.

* Only models of ONNX format are supported with the Predict statement in the Dedicated SQL pool.

* The column names of the scoring input data should match the column names of the model inputs.

* Dedicated SQL pool doesn't support multidimensional array so ensure that the training inputs are individual inputs instead of an array.

## **Recommended Documents**

* [PREDICT (Transact-SQL)](https://docs.microsoft.com/sql/t-sql/queries/predict-transact-sql)

 