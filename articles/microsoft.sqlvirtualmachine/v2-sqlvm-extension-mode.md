<properties
	pageTitle="Register SQL Server virtual machine with latest IaaS extension"
	description="Register SQL Server virtual machine with latest IaaS extension"
	infoBubbleText="Register SQL Server virtual machine with latest IaaS extension"
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
	articleId="0f8a48ac-7e9e-406b-91ce-a7901b06559e-extensionfullmode"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found a recommendation
<!--issueDescription-->
SqlIaaS Extension installed as LightWeight extension.
<!--/issueDescription-->

## **Recommended Steps**
Recommend to register a SQL Server virtual machine in full mode using the [Public article - Register a SQL Server virtual machine in full mode](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash#full-management-mode).Registering in full mode could possibly restart the SQL Server service. Please proceed with caution.