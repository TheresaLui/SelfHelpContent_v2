<properties
  pagetitle="Storage configuration using SQL IaaS Extension "
  description="Storage configuration"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="yareyes,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740103"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="30ad4466-56e3-422f-ab80-45c786b07719"
  ownershipid="AzureData_AzureSQLVM" />
# Storage configuration using SQL IaaS Extension 
 
4 out of 5 customers are able to resolve their Questions and issues with Storage configuration using IaaS Extension using the following steps.  
 
## **Recommended Steps**  
 
SQL Virtual Machine Resource can help you to [Configure your storage/Extend Disks](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#existing-vms) from the Azure portal. Make sure that you have met the **[Pre-requisites](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#prerequisites)**  

 
- **Extend Disk option or Configure blade** on SQL Virtual Machine Resource is dimmed.
 
    - Config Blade can be dimmed if your IaaS Extension is in a failed state. [Please remove and reinstall IaaS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli) 
 
  - Extend Disk option can be dimmed if you have customized your Storage Pool. Increasing a disk size require adding disks to the storage pool and enlarge the virtual disk. 

  - Storage Configuration is expected to have only one virtual disk per storage pool and one volume per virtual disk. Extension will check default naming as `SQLVMStoragePool`, `SQLVMVirtualDisk`, and Volume name to be `SQLVMDATA1`, `SQLVMLOG` and `SQLVMTEMPDB`.  Make sure the names match these default names to resolve this issue. We're working on relaxing the naming constraint to eliminate this problem. 
 
* **SQL Virtual Machine Unavailable/Not Visible** 
 
   [Remove and reinstall IaaS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli) to get the SQL Virtual Machine resource. 
 
- **Disk configuration is dimmed for SQL server while creating the VM with unmanaged disk.** 
 
   This is a default behavior.  
 
* **I have a disk with 1TB of unallocated space that I cannot remove from storage pool** 
 
   Unfortunately there is no option to remove the unallocated space from a disk that belongs to a storage pool. You can manually expand virtual disk and volume space if desired.

* **After uninstalling and reinstalling extension, SQL Server failed to start after VM reboot**
   
     If you use storage configuration to create a VM and allocate temp DB on the D drive, we’ll create a `scheduledTask` to create the folder structure and start SQL Server at OS start up time. Uninstalling the extension will delete this task.  To create the task again run this script in PowerShell:

     ```
      Set-AzureRmVMExtension -ResourceGroupName "{rgName}" -VMName "{vmName}" -Name "SqlIaasExtension" -Publisher 
      "Microsoft.SqlServer.Management" -TypeHandlerVersion "2.0" -ExtensionType "SqlIaaSAgent" -Location " 
      {location}" -SettingString '{"ServerConfigurationsManagementSettings": {"SQLWorkloadTypeUpdateSettings": 
      {"SQLWorkloadType": 1},"SQLStorageUpdateSettingsV2": {"SQLTempDbSettings": {"DefaultFilePath": "D:\\ 
      {temp_db_path}\\"}}}}'
     ``` 

## **Recommended Documents**  
 
* [Configure Storage for existing VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#existing-vms)  
* [Disk Striping](https://docs.microsoft.com/azure/virtual-machines/premium-storage-performance#disk-striping)  
* [Create Storage Pool](https://docs.microsoft.com/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces#step-1-create-a-storage-pool)  
* [How to expand the OS disk of a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)
* [Expand data disks for a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks)
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [Attach an existing disk using the Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) 
* [Detach a data disk using the Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall)
