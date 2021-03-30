<properties
	pageTitle="Diagnose and resolve reportin integration issues with Power BI, Tableau or Qlik"
	description="Diagnose and resolve reportin integration issues with Power BI, Tableau or Qlik"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32784332"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="30543830-8407-47fb-a999-185587622a5f"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve reportin integration issues with Power BI, Tableau or Qlik

## **Recommended Steps**

* To get started, open Power BI Desktop, go to **Get Data** > **Azure**. Select the Azure Databricks connector and provide the Databricks cluster settings. 
To keep the reports and tables already built based on existing sources, perform the migration by editing the data sources in the advanced query editor, using the new connector.

* If you are using Power BI to query data from Azure Databricks, use the newly launched Azure Databricks connector instead of the previous open-source Spark connector. The new connector allows efficient, secure data consumption from Azure Databricks. The new connector leverages Azure AD authentication from Power BI and Azure Databricks. This enables Power BI to use your Azure AD credentials to query and visualize your data in Azure Databricks. Even better, this process is supported with storage credential pass-through and Table ACLs, enabling the viewer to see only the data that the viewer is allowed to see based on Table ACLs or File/Folder ACLs of the underlying storage, with improved performance. The connector, available as part of Power BI Service, also allows the SSO experience for users to access reports. To get started, you need to create the report by using the new connector on Power BI Desktop.

* PowerBI engine is case-insensitive **by design**. For example, it considers "AAA"and "AaA" the same string. This can lead to duplicates. [Learn more](https://blog.crossjoin.co.uk/2019/10/06/power-bi-and-case-sensitivity/), including a workaround to use the Unicode Zero-Width Space character.

* The Azure Databricks connector integrated in Power BI Desktop is in [Public Preview](https://powerbi.microsoft.com/blog/announcing-power-bi-connector-to-azure-databricks-public-preview/). Make sure to upgrade Power BI Desktop to version 2.85.681.0 and above to use it.

## **Recommended Documents**

* [Connect BI tools](https://docs.microsoft.com/azure/databricks/integrations/bi/jdbc-odbc-bi)

	* [Power BI](https://docs.microsoft.com/azure/databricks/integrations/bi/power-bi)
	
	* [Access Azure Databricks using the Power BI Service](https://docs.microsoft.com/azure/databricks/integrations/bi/power-bi#access-azure-databricks-using-the-power-bi-service)
	
	* [Tableau](https://docs.microsoft.com/azure/databricks/integrations/bi/tableau)
	
* [Troubleshooting](https://docs.microsoft.com/azure/databricks/kb/bi/jdbc-odbc-troubleshooting)

* [Accessing secrets with DBUtils fails on Azure Databricks clusters](https://docs.microsoft.com/azure/databricks/kb/bi/dbutils-access-secrets-fails)

