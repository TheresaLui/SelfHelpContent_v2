<properties
	pageTitle="Diagnose and resolve issues with Python"
	description="Diagnose and resolve issues with Python"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677724"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1f3f892a-e17f-4431-9ff2-25cd86d68240"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve Spark issues with Python API (PySpark)

## **Recommended Steps**

* Getting exception **py4j.security.Py4JSecurityException: … is not whitelisted** on High Concurrency cluster with Credential Passthrough enabled - this exception is thrown when you have accessed a method that Azure Databricks has not explicitly marked as safe for Azure Data Lake Storage credential passthrough clusters. In most cases, this means that the method could allow a user on a Azure Data Lake Storage credential passthrough cluster to access another user’s credentials. To resolve issue:
    - You can either disable Credential Passthrough for this HC cluster
    - Or use Standard cluster with Credential Passthrough enabled where single user access is allowed

## **Recommended Documents**

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)
* [How to: Run SQL Queries from Python Scripts](https://docs.microsoft.com/azure/databricks/kb/python/sql-in-python)
* [Reading Large DBFS-Mounted Files Using Python APIs](https://docs.microsoft.com/azure/databricks/kb/python/dbfs-file-size-limit)
* [How to: Create Table DDLs to Import into an External Metastore](https://docs.microsoft.com/azure/databricks/kb/metastore/create-table-ddl-for-metastore)
* [How to: Import a custom CA certificate](https://docs.microsoft.com/azure/databricks/kb/python/import-custom-ca-cert)
* Error: Python Command Execution Fails with AttributeError
     * Resolve this error following the steps in artile: [Python command execution fails with AttributeError](https://docs.microsoft.com/azure/databricks/kb/python/python-command-cancelled)
