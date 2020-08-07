<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738840"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Data Import, Export (ETL) with SQL pool/Using Azure Databricks"
	description = "Data Import, Export (ETL) with SQL pool/Using Azure Databricks"
	articleId = "synapse-dataimportexportetlwithsqlpool-usingazuredatabricks"
	authors = "saltug"
	ms.author = "saltug"
/>

# Data Import, Export (ETL) with SQL pool/Using Azure Databricks

### DataBricks SQL DW Connector: Reading/Writing

* Check your JDBC connection string
* Check your username and password on SQL DW and ensure you can login with that user to your SQL DW
* If you are receiving an error: com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
* Check your permissions. Your SQL DW user needs to have CONTROL permissions to create an external table from SQL DW:

```
    SELECT users.[name], perm.state_desc, perm.permission_name
    FROM sys.database_permissions perm
    JOIN sys.database_principals users ON perm.grantee_principal_id = users.principal_id
    WHERE users.[name] = '<name>'
```

* Check to see if you have spaces in the column names of the table in SQL DW.  Spaces in column names are not supported.  Consider renaming the column removing spaces or use the query option using an alias for column names.

```
    SELECT [My Column Name] AS MyColumnName
    FROM <table>
```

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL pool increases the numbers of readers and writers for parallelism.

## **Recommended Documents**

* [Required SQL Pool Permissions](https://docs.azuredatabricks.net/spark/latest/data-sources/azure/sql-data-warehouse.html#required-sql-dw-permissions)
* [Load data into SQL pool using Azure Databricks](https://docs.microsoft.com/azure/azure-databricks/databricks-extract-load-sql-data-warehouse?toc=/azure/sql-data-warehouse/toc.json)
* [Best practices when loading into SQL Pool](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)


