<properties
	pageTitle="Ensure SqlIaaSExtensionQuery account is added to SQL Server with SysAdmin Permissions"
	description="Ensure SqlIaaSExtensionQuery account is added to SQL Server with SysAdmin Permissions"
	infoBubbleText="Ensure SqlIaaSExtensionQuery account is added to SQL Server with SysAdmin Permissions"
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
	articleId="6767ba94-46e0-42b4-a0c8-51a20a6065de-sqlIaasextensionquery"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found a recommendation

<!--issueDescription-->
[NT SERVICE\SqlIaaSExtensionQuery] account is not added to SQL Server with SysAdmin Permissions.
<!--/issueDescription-->

## **Recommended Steps**

1. **Microsoft SQL Server IaaS Query Service**: Helper service for Microsoft SQL Server IaaS Extension that runs SQL queries against SQL Server on IaaS Virtual Machine and runs as NT Service account.
2. SQL Server IaaS Query Service is started with an NT Service account which is a Sys Admin on the SQL Server. SQL server IaaS Extension is enabling the SQL Server configurations blade on Azure Portal. If you lower the SQL Server permissions for the NT Service\SQLIaaSExtensionQuery account, then you will not be able to successfully use the SQL Server Configurations blade on the portal.
3. Make sure "Microsoft SQL Server IaaS Agent" service is using the [NT Service\SqlIaaSExtensionQuery](https://techcommunity.microsoft.com/t5/sql-server/sql-server-iaas-extension-query-service-for-sql-server-on-azure/ba-p/386015)  account and the account is added to SQL Server as a login with [SysAdmin Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/connect-to-sql-server-when-system-administrators-are-locked-out?view=sql-server-ver15#step-by-step-instructions)


