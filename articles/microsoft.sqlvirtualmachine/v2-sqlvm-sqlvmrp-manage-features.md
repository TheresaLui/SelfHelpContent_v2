<properties
	pageTitle="Manage SQL VM Resource provider and features"
	description="Manage SQL VM Resource provider and features"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="ujpat,vadeveka,amamun"
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740084"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="e4b15454-3556-4186-9793-92c030ff73f8"
	ownershipId="AzureData_AzureSQLVM"
/>

# Manage SQL VM Resource provider and features
## Common Issues

**SQL VM resource status is offline or failed**
<br> Azure Portal may show the following message on the SQL VM resource: *The SQL virtual machine resource is not in a valid state for management. The cause could be the SQL virtual machine is in bad states, the underlying virtual machine state is invalid (Example: stopped, deallocated or failed) or the virtual machine was not found. Please make sure the SQL virtual machine and the underlying virtual machine are healthy.*
<br> The SQL VM resource may be in an unhealthy state if the provisioning of SQL VM failed or if the VM is in an invalid state. If SQL VM resource is unhealthy even after the VM is up and running in a valid state, you can unregister the resource and register again as documented [here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider).  

**SQLIaaSExtension is in a Failed state or stuck in Transitioning state**
<br> Portal may show the following message on the SQL VM resource: *SQL virtual machine management operations are disabled because SQL extension cannot be found or might not be installed properly on the virtual machine.*
<br> The extension may occasionally encounter issues during its workflow resulting in a bad state. Uninstalling and reinstalling the extension should address this issue. 
<br> You can execute the following commands in PowerShell to reinstall the extension:

```
Remove-AzVMSqlServerExtension -ResourceGroupName "<ResourceGroupName>" -VMName "<VMName>" -Name "SqlIaasExtension" 

Set-AzVMExtension -ResourceGroupName "<ResourceGroupName>" -Location "<VMLocation>" -VMName "<VMName>" -Name "SqlIaasExtension" -Publisher "Microsoft.SqlServer.Management" -ExtensionType "SqlIaaSAgent" -TypeHandlerVersion "2.0";
```
**Cannot disable Automated Patching/Managed Backup**

Check if you see the SQLIaasExtension on the portal in provisioning succeeded state. 
- If yes, then please see if you can see any error in the extension log at: C:\Users\ujpat\Desktop\Microsoft.Powershell.DSC\WindowsAzure\Logs\Plugins\Microsoft.SqlServer.Management.SqlIaaSAgent\1.2.24.0\ ExtensionLog_0.log
- Else try to remove and re-install IAAS Agent extension.

## **Recommended Documents**
* [Register a SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider?tabs=azure-cli%2Cbash)
* [Bulk register SQL virtual machines in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-bulk-register-with-resource-provider)
* [Automate management tasks on Azure Virtual Machines with the SQL Server Agent Extension Resource Manager](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension)

