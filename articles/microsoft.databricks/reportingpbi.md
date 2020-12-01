<properties
	pageTitle="Diagnose and resolve reportin integration issues with Power BI, Tableau or Qlik"
	description="Diagnose and resolve reportin integration issues with Power BI, Tableau or Qlik"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677723"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="30543830-8407-47fb-a999-185587622a5f"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve reportin integration issues with Power BI, Tableau or Qlik

## **Recommended Steps**

* PowerBI engine is case insensitive **by design**, so for example, it would consider "AAA"and "AaA" the same string. This can ead to duplicates. [Learn more](https://blog.crossjoin.co.uk/2019/10/06/power-bi-and-case-sensitivity/), including a workaround to use the Unicode Zero-Width Space character.

* The Azure Databricks connector integrated in Power BI Desktop is in [Public Preview](https://powerbi.microsoft.com/blog/announcing-power-bi-connector-to-azure-databricks-public-preview/). Please make sure to upgrade Power BI Desktop to version 2.85.681.0 and above to use it.

## **Recommended Documents**

* [Connect BI tools](https://docs.microsoft.com/azure/databricks/integrations/bi/jdbc-odbc-bi)

	* [Power BI](https://docs.azuredatabricks.net/user-guide/bi/power-bi.html)
	
	* [Tableau](https://docs.microsoft.com/azure/databricks/integrations/bi/tableau)
	
* [Troubleshooting](https://docs.microsoft.com/azure/databricks/kb/bi/jdbc-odbc-troubleshooting)

* [Accessing secrets with DBUtils fails on Azure Databricks clusters](https://docs.microsoft.com/azure/databricks/kb/bi/dbutils-access-secrets-fails)

