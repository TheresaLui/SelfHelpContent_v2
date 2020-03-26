<properties
  pageTitle="tools and portal/azure portal"
	description="tools and portal/azure portal"
	infoBubbleText=""
	service="microsoft.compute"
	resource="virtualmachines"
	authors="vadeveka"
	ms.author="vadeveka"
	displayOrder=""
	articleId="sqlvirtualmachine-tools and portal-azure portal"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32633494"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public,fairfax"
	ownershipId="AzureData_AzureSQLVM"
/>

# tools and portal/azure portal

Most users are able to resolve the errors on SQL Virtual Machine resource in Azure Portal using the recommend steps listed below.

* **The SQL virtual machine resource is not in a valid state for management. The cause could be the SQL virtual machine is in bad states, the underlying virtual machine state is invalid (Example: stopped, deallocated or failed) or the virtual machine was not found. Please make sure the SQL virtual machine and the underlying virtual machine are healthy.**

  The SQL VM resource may be in an unhealthy state if the provisioning of SQL VM failed or if the VM is in an invalid state. If SQL VM resource is unhealthy even after the VM is up and running in a valid state, you can unregister the resource and register again as documented [here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider). You can choose to re-register it in Lightweight mode first and then upgrade to Full during a scheduled downtime. 

* **SQL virtual machine management operations are disabled because SQL extension cannot be found or might not be installed properly on the virtual machine.**

  The SQL IaaS extension may occasionally encounter issues during its workflow resulting in a bad state. Uninstalling and installing the extension should address this issue. 

  You can execute the following commands in PowerShell to re-install the extension:

  ```
  Remove-AzVMSqlServerExtension -ResourceGroupName "<ResourceGroupName>" -VMName "<VMName>" -Name "SqlIaasExtension" 

  Set-AzVMExtension -ResourceGroupName "<ResourceGroupName>" -Location "<VMLocation>" -VMName "<VMName>" -Name "SqlIaasExtension" -Publisher "Microsoft.SqlServer.Management" -ExtensionType "SqlIaaSAgent" -TypeHandlerVersion "2.0";
  ```

## **Recommended Documents**

* [SQL Virtual Machine registration and FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
* [Automate management tasks on Azure Virtual Machines with the SQL Server Agent Extension](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension)
