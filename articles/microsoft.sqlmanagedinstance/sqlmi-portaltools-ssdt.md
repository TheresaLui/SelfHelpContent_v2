<properties
	pageTitle="Portal and Client Tools/SQL Server Data Tools (SSDT)"
	description="Portal and Client Tools/SQL Server Data Tools (SSDT)"
	infoBubbleText="Portal and Client Tools/SQL Server Data Tools (SSDT)"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637307"
	resourceTags=""	
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="d4a00f3b-45d8-4dcd-8779-671ad39f67c6"
	ownershipId="AzureData_AzureSQLMI"
/>

# SQL Server Data Tools

SQL Server Data Tools (SSDT) is a modern development tool for building Azure SQL Managed Instance relational databases. SSDT is supported for Managed Instance since Visual Studio 2019 with some limitations as follows:

* Using Azure AD server principals (logins) and users with SQL Server Data Tools currently isn't supported with SSDT.
* Scripting for Azure AD server principals (logins) and users isn't supported in SSDT.

## **Recommended Steps**

* Ensure you are running Visual Studio 2019, or higher.
* Ensure you are using the latest version of SQL Server Data Tools, as older version than 2019 will not work with Managed Instance. [Download here](https://visualstudio.microsoft.com/vs/features/ssdt/).
* Ensure you are not using Azure AD logins with SSDT as this is not supported at this time.

## **Recommended Documents**

* To learn more about SSDT, see [SQL Server Data Tools](https://docs.microsoft.com/sql/ssdt/sql-server-data-tools)
