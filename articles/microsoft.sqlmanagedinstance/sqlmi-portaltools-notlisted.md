<properties
	pageTitle="Portal and Client Tools/My issue is not listed"
	description="Portal and Client Tools/My issue is not listed"
	infoBubbleText="Portal and Client Tools/My issue is not listed"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637285"
	resourceTags=""	
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="476e5ba5-cb1c-41d8-80ce-ccafd261c5bc"
	ownershipId="AzureData_AzureSQLMI"
/>

# Portal Tools - My issue is not listed

Managed Instance supports a number of tools listed below.

## **Recommended Steps**

Ensure you are using the latest version of tools for  Managed Instance. To connect to Managed Instance, consider using the following tools:

* [SQL Server Data Tools for Visual Studio (SSDT)](https://docs.microsoft.com/sql/ssdt/sql-server-data-tools). Note that Visual Studio 2019 or higher is required.
* [SQL Server Management Studio (SSMS)](https://docs.microsoft.com/sql/ssms/sql-server-management-studio-ssms). Note that SSMS version 18 or higher is required.

Please note that Query Editor in Azure Portal is not supported for Managed Instance. This is due to security constraints of Managed Instance being enclosed in private VNet due to which external Query Editor cannot connect to Managed Instance.

## **Recommended Documents**

* [Managed Instance quickstart guide](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-quickstart-guide)
