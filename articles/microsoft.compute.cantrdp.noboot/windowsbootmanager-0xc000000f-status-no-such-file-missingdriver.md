<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot with error code 0xc000000F"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="Ram-Kakani,timbasham"
    ms.author="ramak,tibasham"
    displayOrder=""
    articleId="WindowsBootManager-0xC000000F-STATUS_NO_SUCH_FILE-MissingDriver"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error
<!--issueDescription-->
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->[vmname]<!--/$vmname-->. We identified that your VM is currently in an inaccessible state because Windows failed to boot with error code **0xc000000f**. This issue occurs when a device that doesn't exist is specified in the Boot Configuration data.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To fix the BCD store, follow the troubleshooting steps indicated below:

1. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. **Make sure that you select the "Keep the disks" option when you do this**.
2. Before proceeding further, save a copy of the OS disk. This will help in case of a rollback for recovery. See [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/vhd-copy).
3. Attach the OS disk of the deleted VM as a data disk to a troubleshooting VM. For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal).
4. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned
5. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition:

  * The Windows partition contains a folder named "Windows," and this partition is larger than the others
  * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB.

6. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. You will use this identifier in the next step:

```
bcdedit /store [Boot partition]:\boot\bcd /enum
```

7. Repair the Boot Configuration data by running the following command lines. You must replace these placeholders by the actual values:

  * "Windows partition" is the partition that contains a folder named "Windows."
  * "Boot partition" is the partition that contains a hidden system folder named "Boot."
  * "Identifier" is the identifier of Windows Boot Loader you found in the previous step.

```
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} device partition=[boot partition]:
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} integrityservices enable
bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} device partition=[Windows partition]:
bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} integrityservices enable
bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} recoveryenabled Off
bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} osdevice partition=[Windows partition]:
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
```

8. Detach the repaired OS disk from the troubleshooting VM. [Then, create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized).
