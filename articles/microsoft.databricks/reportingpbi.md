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

* PowerBI engine is case insensitive **by design** so it would consider 'AAA' and 'AaA' the same string which may lead to duplicates. This [blog](https://blog.crossjoin.co.uk/2019/10/06/power-bi-and-case-sensitivity/) goes into more details and has a workaround to use the Unicode Zero-Width Space character.

## **Recommended Documents**

* [Power BI](https://docs.azuredatabricks.net/user-guide/bi/power-bi.html)
