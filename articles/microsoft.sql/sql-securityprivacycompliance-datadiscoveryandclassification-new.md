<properties
	pageTitle="security, privacy and compliance/data discovery and classification"
	description="security, privacy and compliance/data discovery and classification"
	service="microsoft.sql"
	resource="servers"
	authors="sojaga,bashahee"
    ms.author="sojaga,bashahee"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630416"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="9345d055-93c1-4f7c-8978-627cb70cea3f"
	ownershipId="AzureData_AzureSQLDB_Security"
/>

# Data Discovery and Classification

Data Discovery & Classification is built into Azure SQL Database, Azure SQL Managed Instance, and Azure Synapse Analytics. It provides basic capabilities for discovering, classifying, labeling, and reporting the sensitive data in your databases.

## Recommended Steps
-	Use [Azure Portal.](https://docs.microsoft.com/azure/azure-sql/database/data-discovery-and-classification-overview#discover-classify-columns)
 or [SQL Server Management Studio SSMS.](https://docs.microsoft.com/sql/relational-databases/security/sql-data-discovery-and-classification?view=sql-server-ver15&tabs=t-sql#Manage-information-protection-policy-with-SSMS)

### Manage classifications
-	Use [T-SQL.](https://docs.microsoft.com/azure/azure-sql/database/data-discovery-and-classification-overview#use-t-sql)
-	Use [PowerShell Cmdlets.](https://docs.microsoft.com/azure/azure-sql/database/data-discovery-and-classification-overview#use-powershell-cmdlets)
-	Use [REST-APIs.](https://docs.microsoft.com/azure/azure-sql/database/data-discovery-and-classification-overview#use-the-rest-api)

### Permissions needed for Data Classification
-	Read about permissions and access needed for enable/setup data classification for a database: [Owner.](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner), [Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#reader)
, [Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor), [SQL Security Manager](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-security-manager)
•	[User Access Administrator](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#user-access-administrator)
-	To Modify data classification of a database permissions and access needed:
•	[Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner)
•	[Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor)
•	[SQL Security Manager](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-security-manager)

### FAQ
- Q.	Will [Azure Purview](https://docs.microsoft.com/azure/purview/overview) replace SQL Data Discovery & Classification or will SQL Data Discovery & Classification be retired soon?
<br>A.	We continue to support SQL Data Discovery & Classification and encourage you to adopt [Azure Purview](https://docs.microsoft.com/azure/purview/overview) which has richer capabilities to drive advanced classification capabilities and data governance. If we decide to retire any service, feature, API or SKU, you will receive advance notice including a migration or transition path. Learn more about Microsoft Lifecycle policies here.
- Q.	How to classify my Azure SQL data using Azure Purview labels?
<br>A.	Please follow these [steps](https://docs.microsoft.com/azure/sql-database/scripts/sql-database-import-purview-labels).
- Q.	How to dismiss all recommendations for a given Azure SQL Database?
<br>A.  Please run this [PowerShell Command](https://docs.microsoft.com/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation?view=azps-5.5.0#example-2--disable-sensitivity-recommendations-on-columns-which-have-sensitivity-recommendations-in-an-azure-sql-database-using-piping-)

## **Recommended Documents**

### Data Classificiation Videos on setup and overview
* [Demo Data Classification](https://youtu.be/_aJiFzyPfnE)
* [Overview of Data Classification](https://youtu.be/itVi9bkJUNc)

### Data Classification documentation on setup and overview
* [Data discovery and classification](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification?WT.mc_id=pid:13491:sid:32630416/)<br>
* [Advanced Threat Protection](https://docs.microsoft.com/azure/sql-database/sql-advanced-threat-protection?WT.mc_id=pid:13491:sid:32630416/)
