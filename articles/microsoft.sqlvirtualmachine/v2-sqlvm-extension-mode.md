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
SQL IaaS Agent Extension is registered in Lightweight mode which enables limited functionality. Consider upgrading to Full mode to enable additional functionality.
<!--/issueDescription-->

## **Recommended Steps**

Learn more about the SQL IaaS Agent Extension management modes [here](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-server-iaas-agent-extension-automate-management?tabs=azure-powershell#management-modes). We recommend registering a SQL Server virtual machine in Full mode if possible. Follow [these instructions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli#full-management-mode) to upgrade to Full mode, keeping in mind that moving from Lightweight to Full mode will trigger a restart of the SQL Server service.

**Note:** Registering in full mode will restart the SQL Server service. Please proceed with caution.
