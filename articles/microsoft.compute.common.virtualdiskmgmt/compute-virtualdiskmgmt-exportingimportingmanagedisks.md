<properties
	pagetitle="Solutions for exporting/importing managed disks"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="ramankum"
	selfhelptype="Generic"
	supporttopicids="32747646"
	productpesids="15571,15797,16454,16470,14749"
	cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
	articleid="a00e3c31-f2a7-4d5d-ba24-160667784f7d"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Solutions for exporting/importing managed disks

Want a solution right now?

Try following the recommended steps below. These solutions are written by Azure engineers, and will solve most common issues.

## **Recommended Steps**

1. Export/Copy a snapshot to a storage account using [CLI](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-cli-sample-copy-snapshot-to-storage-account?toc=/azure/virtual-machines/linux/toc.json) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-powershell-sample-copy-snapshot-to-storage-account)
2. Export/Copy a managed disk to a storage account using [CLI](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-cli-sample-copy-managed-disks-vhd) or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-powershell-sample-copy-managed-disks-vhd)
3. [Upload a vhd to Azure using Azure PowerShell and AzCopy v10](https://docs.microsoft.com/azure/virtual-machines/windows/disks-upload-vhd-to-managed-disk-powershell)
4. [Upload a vhd to Azure using Azure CLI and AzCopy v10](https://docs.microsoft.com/azure/virtual-machines/linux/disks-upload-vhd-to-managed-disk-cli)
5. [Upload, download, cross-region copy managed disks using Azure Storage Explorer](https://docs.microsoft.com/azure/virtual-machines/windows/disks-use-storage-explorer-managed-disks)
6. Securely export/import managed disks via Private Links using [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/disks-export-import-private-links-cli) or the [Portal](https://docs.microsoft.com/azure/virtual-machines/disks-enable-private-links-for-import-export-portal?toc=/azure/virtual-machines/linux/toc.json&bc=/azure/virtual-machines/linux/breadcrumb/toc.json)

## **Recommended Documents**

* [FAQ for securely exporting and importing Managed Disks via Private Links](https://docs.microsoft.com/azure/virtual-machines/faq-for-disks#private-links-for-securely-exporting-and-importing-managed-disks)