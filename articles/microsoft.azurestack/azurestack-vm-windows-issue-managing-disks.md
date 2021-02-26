<properties
  pagetitle="Issues with attaching and detaching disks in Windows VM&#xD;"
  service="microsoft.azurestack"
  resource="azurestack"
  ms.author="mquian,mabrigg"
  selfhelptype="Generic"
  supporttopicids="32663908,32663910"
  resourcetags=""
  productpesids="16226"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="6f641910-1010-4135-b8d1-85ab25fa1503"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Issues with attaching and detaching disks in Windows VM

Before you try to detach a disk, connect to the VM and unmount it.

Most users were able to resolve issues by using the following steps.

## **Recommended Steps**

- Attach a new disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#attach-a-new-disk) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps) 
- [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal)
- Attach an existing disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps)
- Detach a data disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portal) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell) 
- [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)
- [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)
- [Use the D: drive as a data drive on a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter)
- [Convert an unmanaged disk to a managed disk](https://docs.microsoft.com/azure-stack/user/azure-stack-managed-disk-considerations#convert-to-managed-disks)

## **Recommended Documents**

- [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
- [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/convert-unmanaged-to-managed-disks)
- [Convert to managed disks](https://docs.microsoft.com/azure-stack/user/azure-stack-managed-disk-considerations#convert-to-managed-disks)
- If you can't attach your SSD disk to a VM, it is likely a VM that doesn't support a premium disk. For more detail about the VM sizes which support premium storage, refer to [Sizes for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/sizes).
