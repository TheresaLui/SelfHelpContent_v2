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
	articleId="bce6aced-6883-4a74-836c-b79be5030954-extensionmissing"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
SQL IaaS Agent Extension is missing.
<!--/issueDescription-->

## **Recommended Steps**

We recommend to unregister and register with SQL IaaS Agent Extension, following [these instructions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm).
