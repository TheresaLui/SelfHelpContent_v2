<properties
	pageTitle="Databricks DBFS and Database Issues"
	description="Databricks DBFS and Database Issues"
	service="microsoft.Databricks"
	resource="workspaces"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612191"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="40cf8bd8-e8e7-4632-a1b9-d8a238140f5b"
	ownershipId="AzureData_AzureDatabricks"
/> 

# Azure Databricks DBFS and Database

## **Recommended steps**

- Run the [following command](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html#access-dbfs-with-dbutils) in any cell of your notebook to see all the commands available to manage your Databricks File System (DBFS): dbutils.fs.help()
- When using [Spark APIs](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html#access-dbfs-using-spark-apis) in your notebook, reference files with "/mnt/training/file.csv" or "dbfs:/mnt/training/file.csv"
- When using [local file APIs](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html#access-dbfs-using-local-file-apis) in your notebook, you must provide the path under /dbfs, for example: "/dbfs/mnt/training/file.csv"
- Local file I/O APIs only support files less than 2GB in size. Access files larger than 2GB using the DBFS CLI, dbutils.fs, or Spark APIs
- If you write a file using the local file I/O APIs and then immediately try to access it using the DBFS CLI, dbutils.fs, or Spark APIs, you might encounter a FileNotFoundException, a file of size 0, or stale file contents. To force those writes to be flushed to persistent storage (in our case DBFS), use the standard Unix system call sync

## **Recommended documents**

1. [Databricks File System](https://docs.azuredatabricks.net/user-guide/dbfs-databricks-file-system.html)
2. [Databricks Concepts](https://docs.azuredatabricks.net/getting-started/concepts.html)
3. [Databricks DBFS CLI](https://docs.databricks.com/user-guide/dev-tools/databricks-cli.html#dbfs-cli)
4. [Mount Azure Blob Storage to DBFS](https://docs.databricks.com/spark/latest/data-sources/azure/azure-storage.html)
