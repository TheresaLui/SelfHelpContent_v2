<properties
    pageTitle="Azure Stack Issues with attaching and detaching disks in Linux VM"
    description="Azure Stack cannot connect to Linux VM"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663907,32663909"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="6f641910-1002-4135-b8d1-85ab25fa1503"
/>

# Issues with attaching and detaching disks in Linux VM

## **Recommended Steps**

- Attach a new disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)
- [Initialize a new data disk in a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#connect-to-the-linux-vm-to-mount-the-new-disk)
- Attach an existing disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)
- Detach a data disk using the [Azure portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli) 
- [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)
- [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)

NOTE: When you detach a disk, remember to connect to the VM and unmount the disk first. 

## **Recommended Documents**

- [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
- [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#features)
- [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)
- [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#premium-disks-managed-and-unmanaged)
- [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)
