<properties
	pageTitle="sql administration/sql iaas extension"
	description="sql administration/sql iaas extension"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32633515"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	articleId="5ab8e128-ff65-45d6-a0f4-9a4f44cce799"
	ownershipId="AzureData_AzureSQLVM"
/>

# sql administration/sql iaas extension

* **SQLIaaSExtension is in a Failed state or stuck in Transitioning state**

Portal may show the following message on the SQL VM resource: *SQL virtual machine management operations are disabled because SQL extension cannot be found or might not be installed properly on the virtual machine.*

The extension may occasionally encounter issues during its workflow resulting in a bad state. Un-installing and installing the extension should address this issue. 

You can execute the following commands in PowerShell to re-install the extension:

```
Remove-AzVMSqlServerExtension -ResourceGroupName "<ResourceGroupName>" -VMName "<VMName>" -Name "SqlIaasExtension" 

Set-AzVMExtension -ResourceGroupName "<ResourceGroupName>" -Location "<VMLocation>" -VMName "<VMName>" -Name "SqlIaasExtension" -Publisher "Microsoft.SqlServer.Management" -ExtensionType "SqlIaaSAgent" -TypeHandlerVersion "2.0";
```

* **SQL VM resource status is offline or failed**

Azure Portal may show the following message on the SQL VM resource: *The SQL virtual machine resource is not in a valid state for management. The cause could be the SQL virtual machine is in bad states, the underlying virtual machine state is invalid (Example: stopped, deallocated or failed) or the virtual machine was not found. Please make sure the SQL virtual machine and the underlying virtual machine are healthy.*

The SQL VM resource may be in an unhealthy state if the provisioning of SQL VM failed or if the VM is in an invalid state. If SQL VM resource is unhealthy even after the VM is up and running in a valid state, you can unregister the resource and register again as documented [here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider).  

## **Recommended Documents**

* [Automate management tasks on Azure Virtual Machines with the SQL Server Agent Extension Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension)
