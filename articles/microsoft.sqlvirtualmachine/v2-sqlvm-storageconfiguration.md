<properties
  pagetitle="Storage configuration using SQL IaaS Extension &#xD;"
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

Most users are able to resolve issues concerning storage configuration using IaaS Extension by using the following steps.  

## **Recommended Steps**  

  **SQL Virtual Machine Resource can help you to [Configure your storage/Extend Disks](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#existing-vms) from Azure portal**  
<Br>  

- **Extend Disk option or Configure blade** on SQL Virtual Machine Resource is **Grayed Out**  

    - Config Blade can be grayed out if your IaaS Extension is in a failed state. [Remove and reinstall IaaS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli) 

    - Extend Disk option can be grayed out if you've customized your Storage Pool. Increasing a disk size requires adding disks to the storage pool and enlarging the virtual disk. 

* **SQL Virtual Machine is Unavailable/Not Visible** 

   [Remove and reinstall IaaS Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli) to get the SQL Virtual Machine resource. 

- **Disk configuration grayed out for SQL server while creating the VM with unmanaged disk.** 

   This is a default behavior.  

* **I have a disk with 1TB of unallocated space that I cannot remove from storage pool** 

   There is no option to remove the unallocated space from a disk that belongs to a storage pool. 

## **Recommended Documents**  

* [Configure Storage for existing VMs](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/storage-configuration#existing-vms)  
* [Disk Striping](https://docs.microsoft.com/azure/virtual-machines/premium-storage-performance#disk-striping)  
* [Create Storage Pool](https://docs.microsoft.com/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces#step-1-create-a-storage-pool)  
* [How to expand the OS disk of a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)
* [Expand data disks for a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks)
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [Attach an existing disk using the portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) 
* [Detach a data disk using the portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall)
