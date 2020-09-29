<properties
  pagetitle="SQL VM Resource provider or IaaS Extension "
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740084"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="e4b15454-3556-4186-9793-92c030ff73f8"
  ownershipid="AzureData_AzureSQLVM" />
# SQL VM Resource provider or IaaS Extension 

 SQL Resource Provider and its features are free for use. Most of the SQL VM Resource provider or IAAS Extension issues are fixed by uninstalling and reinstalling it.

## **Recommended Steps**

* **Notifications for Resource Provider Auto Registration**

  * Registering with SQL VM RP will enable enhanced monitoring and management, flexible license and edition conversions, and asset discovery benefits with no impact on existing resources
   * There is no impact. IAAS Extension will get installed in lightweight mode which does not require any service/VM Restart. All SQL Server instances installed from SQL Server 2016 or above versions will be target for this maintenance globally.

* **SQL management operations are disabled because the state of underlying virtual machine is invalid**

   * You may see this if SQL VM is stopped, deallocated or failed or the VM was not found. Please make sure the SQL virtual machine and the underlying virtual machine is running. This may also happen if IAAS Extension is in failed state. [Remove and Reinstall the IAAS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-server-iaas-agent-extension-automate-management)
   * This may happen if you migrated your VM from one subscription or resource group to other. To fix this, you can [Unregister the  SQL VM Resource Provider and Register again](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider).  
   * You may see this if you have changed the SQL Locale. To fix this, you can [Unregister the  SQL VM Resource Provider and Register again](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash#unregister-from-rp).  

* **SQL IAAS Extension does not show up "Provisioning Succeeded" on Azure Portal**
 
  * If you see any login failures for **NT SERVICE\SqlIaaSExtensionQuery**, please make sure this account is added to SQL Server with **SysAdmin** Permissions
  * Check for the task scheduler jobs **"RunConfigureImage" or "IsSqlScheduledSetupCompleted"** if in a failed state. Delete these jobs and [Reinstall the extension](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension) or follow the FAQ "[How do I generalize SQL Server on Azure VM and use it to deploy new VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/frequently-asked-questions-faq#images)".
  * Remove and [Reinstall the Extension](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension)

* **Common Issues with Managing SQL VM Resource Provider Resource and IAAS Extension**
    
  * [Lightweight mode of IAAS Extension does not offer the full capability of IAAS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash#management-modes). Hence, you may see other features are grayed out. This also applies to SQL FCI because only lightweight mode is supported on FCI for now.
  * If you do not see a SQL VM Resource Provider, you can register the [SQL VM Resource Provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider)
  * We recommend to Unregister and again Register the SQL VM Resource provider after you change your SQL Version/Edition for the correct reflection of the billing and Resource validation
  * Storage Configuration or Extending drives from SQL Resource provider may be greyed out if you have customized your storage pool

* **My C Drive is having space issues and IAAS Extension in a failed state and Event viewer logs shows "SQL Server Scheduled Setup is still in progress..."**

  * To fix this, delete the Task scheduler job "RunConfigureImage","IsSqlScheduledSetupCompleted" or follow the FAQ "[How do I generalize SQL Server on Azure VM and use it to deploy new VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/frequently-asked-questions-faq#images)"

## **Recommended Documents**

* [Register or Unregister a SQL Server virtual machine in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-register-with-resource-provider?tabs=azure-cli%2Cbash)
* [Bulk register SQL virtual machines in Azure with the SQL VM resource provider](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-bulk-register-with-resource-provider)
* [Automate management tasks , Install or Remove IAAS Extension on Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-agent-extension)
* [Configure Storage from SQL Resource Provider]( https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#existing-vms)
* [Benefits of SQL RP Registration](https://techcommunity.microsoft.com/t5/sql-server/benefit-from-resource-provider-registration-when-self-installing/ba-p/742794)
