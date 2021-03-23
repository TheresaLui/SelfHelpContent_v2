<properties
	pageTitle="IAAS extension in transitioning state"
	description="IAAS extension in transitioning state"
	infoBubbleText="IAAS extension in transitioning state"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740102"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="ae381cce-58b3-4690-b8b1-5532c8230cf4-extensionintransitionstate"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found a recommendation

<!--issueDescription-->
You are trying to install SQL Server extension on a virtual machine that has SQL 2017 developer edition installed and it is getting stuck in "Transitioning state" [{"version":1.0,"timestampUTC":"6/14/2018 5:05:34 PM","status":{"name":"Microsoft.SqlServer.Management.SqlIaaSAgent","operation":"Enabling Handler","status":"Transitioning"}}]
<!--/issueDescription-->

## **Recommended Steps**

1. Based on the symptoms and analysis of logs it looks like there are some permission issues for the account running SQL Server IaaS extension service that prevented it from properly communicating with the services control manager.
2. Adding the NT service\SQLIaasExtension account to the local administrators group resolved the issue. Make sure "Microsoft SQL Server IaaS Agent" service is using the [NT Service\SqlIaaSExtensionQuery](https://techcommunity.microsoft.com/t5/sql-server/sql-server-iaas-extension-query-service-for-sql-server-on-azure/ba-p/386015)  account and the account is added to SQL Server as a login with [SysAdmin Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/connect-to-sql-server-when-system-administrators-are-locked-out?view=sql-server-ver15#step-by-step-instructions)


