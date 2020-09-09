<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SQLDataWarehouse"
    service = "microsoft.synapse"
    resource = ""
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32743061"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Data Import, Export (ETL) with SQL pool/Loading Machine Learning Models"
    description = "Data Import, Export (ETL) with SQL pool/Loading Machine Learning Models"
    articleId = "synapse-dataimportexportetlwithsqlpool-loadingmachinelearningmodels.md"
    authors = "saltug"
    ms.author = "saltug"
/>

# Data Import, Export (ETL) with SQL pool/Loading Machine Learning Models

## **Recommended Steps**
* A model is saved in a table with varbinary(max) data type
* Model can be loaded into a data warehouse just like any varbinary(max) data is loaded. You can use Copy command or Polybase.
* Apps such as Netron can be used to visualize the model outside the data warehouse
* Only models of ONNX format are supported. Make sure to convert the model into a hex string before loading.


## **Recommended Documents**
* [PREDICT (Transact-SQL)](https://docs.microsoft.com/sql/t-sql/queries/predict-transact-sql)