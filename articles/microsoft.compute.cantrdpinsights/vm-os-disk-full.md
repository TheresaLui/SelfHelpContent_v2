<properties
    pageTitle="VM OS disk full"
    description="Virtual machine has a full OS disk"
    infoBubbleText="We have detected that your VM has a full OS disk."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="vm_osdiskfull"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Virtual machine has a full OS disk

<!--issueDescription-->
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state because the OS disk is full.

If you find that you can't connect to a VM in the future, view a screenshot of your VM using the boot diagnostics blade in the Azure portal. This can help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**

### Free up disk space

1. If the disk size is below 1 TB, expand it up to a maximum of 1 TB [using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)
1. If the disk is already 1 TB, you will need to perform a disk cleanup
    1. Use the [Disk Cleanup tool](https://support.microsoft.com/windows/disk-cleanup-in-windows-10-8a96ff42-5751-39ad-23d6-434b4d5b9a68) to free up space
1. After resizing and clean-up are finished, defragment the drive by using the following command:

```
defrag <LETTER ASSIGN TO THE OS DISK>: /u /x /g
```

Depending upon the level of fragmentation, defragmentation could take several hours.
