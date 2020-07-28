<properties
	pageTitle="SQL VM Resource provider or IaaS Extension setup"
	description="SQL VM Resource provider or IaaS Extension setup"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740102"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="2c2e2bf6-60c9-4adf-aee7-cdc04adbcf26"
	ownershipId="AzureData_AzureSQLVM"
/>

# SQL VM Resource provider or IaaS Extension setup

If you are planning to deploy a SQL inside a Virtual Machine, follow the [Provision SQL Server using Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision) guide.

## Common Issues

* **SQL VM resource status is offline or failed**
	
	Azure Portal may show the following message on the SQL VM resource: *The SQL virtual machine resource is not in a valid state for management. The cause could be the SQL virtual machine is in bad states, the underlying virtual machine state is invalid (Example: stopped, deallocated or failed) or the virtual machine was not found. Please make sure the SQL virtual machine and the underlying virtual machine are healthy.*
	
	The SQL VM resource may be in an unhealthy state if the provisioning of SQL VM failed or if the VM is in an invalid state. If SQL VM resource is unhealthy even after the VM is up and running in a valid state, you can unregister the resource and register again as documented [here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider).  

* **SQLIaaSExtension is in a Failed state or stuck in Transitioning state**

	Portal may show the following message on the SQL VM resource: *SQL virtual machine management operations are disabled because SQL extension cannot be found or might not be installed properly on the virtual machine.*

The extension may occasionally encounter issues during its workflow resulting in a bad state. Uninstalling and reinstalling the extension should address this issue. You can execute the following commands in PowerShell to re-install the extension:

```
Remove-AzVMSqlServerExtension -ResourceGroupName "<ResourceGroupName>" -VMName "<VMName>" -Name "SqlIaasExtension"

Set-AzVMSqlServerExtension -VMName "<VMName>" -ResourceGroupName "<ResourceGroupName>" -Name "SQLIaasExtension" -Version "2.0" -Location "<VMLocation>"
```

## **Recommended Documents**

* [Register a SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider?tabs=azure-cli%2Cbash)
* [Bulk register SQL virtual machines in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-bulk-register-with-resource-provider)
* [Automate management tasks on Azure Virtual Machines with the SQL Server Agent Extension Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension)

