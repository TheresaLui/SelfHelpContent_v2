<properties
	pageTitle="Tools/DepOps tools"
	description="Tools/DepOps tools"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637239"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="f9ded5d7-a69b-4268-a394-9d3372bdf746"
	ownershipId="AzureData_AzureSQLMI"
/>

# SQL Server Management Studio and tools

Managed Instance enables you to use a variety of DevOps tools such as Azure CLI, Azure PowerShell, and Azure Resource Manager Templates.

## **Recommended Steps**

- Check are you using the latest version of Azure CLI, Azure PowerShell, SQL Server Management Studio (18 or higher), SQL Server Data Tools, SQL Server Management Objects (15 or higher).
- If you are getting connection timeout, note that some of the operations are long-running. Use parameter **-AsJob** in the commands like [New-AzResourceGroupDeployment](https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroupdeployment).
- Make sure that the account that is performing the action has the required Azure RBAC permissions. The recommended RBAC role is [SQL Managed Instance Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-managed-instance-contributor)
- Check are there any [known issues](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information) that are reported.

## **Recommended Documents**

- [Azure CLI samples](https://docs.microsoft.com/azure/sql-database/sql-database-cli-samples).
- [Azure PowerShell samples](https://docs.microsoft.com/azure/sql-database/sql-database-powershell-samples).
- [Azure Resource Manager samples](https://docs.microsoft.com/azure/sql-database/sql-database-resource-manager-samples).
