<properties
    pageTitle="Azure Stack Issues with attaching and detaching disks in Windows VM"
    description="Azure Stack cannot connect to Windows VM"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663908,32663910"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="6f641910-1010-4135-b8d1-85ab25fa1503"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Issues with attaching and detaching disks in Windows VM

## **Recommended Steps**

- Attach a new disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#attach-a-new-disk) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps). 
- [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal).
- Attach an existing disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps).
- Detach a data disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portal) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell) .
- [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks).
- [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk).

NOTE: When you detach a disk, remember to connect to the VM and unmount the disk first.

## **Recommended Documents**

- [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
- [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
- [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)
- [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/convert-unmanaged-to-managed-disks)