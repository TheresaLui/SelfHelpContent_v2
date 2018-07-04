<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot with a Bitlocker Key prompt"
    infoBubbleText="A boot error 'Plug in the USB drive that has the Bitlocker key' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ram-kakani"
    displayOrder=""
    articleId="BootError-BITLOCKER"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM boot error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because windows failed to boot with error code **Plug in the USB drive that has the Bitlocker key**.

This behavior is observed if the process of retrieving the BEK files from the BEK volume on Azure platform has encountered issues while starting a VM using the [Azure Disk Encryption extension](https://docs.microsoft.com/azure/security/azure-security-disk-encryption).

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To restore the VM follow the below steps:
1. Stop de-allocate and start the Virtual Machine <!--$vmname-->[vmname]<!--/$vmname--> to check if issue persists.
2. If the VM still fails to boot, delete the VM selecting the Keep the disks option.
3. Before proceeding further save a copy of the OS disk, this will help in case of a rollback for recovery, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
4. Attach the copy/snapshot of the OS disk of the VM as a data disk to another VM (a troubleshooting VM) that is using Azure Disk Encryption Extension. For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
5. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
6. Now to unlock the encrypted drive follow the steps in this  [article](https://blogs.msdn.microsoft.com/mast/2016/11/27/azure-disk-encryption-how-to-recover-bek-file-from-azure-key-vault/).
7. If desired now is a good time to enable your Windows VM to use Azure Serial Console which can help in diagnosing and resolving future issues. [Virtual machine serial console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console), otherwise skip to the step 11 to restore the VM with the unlocked OS disk.
8. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step
      ```
      bcdedit /store [Boot partition]:\boot\bcd /enum
      ```
10. Enable Azure Serial Console by running the following command lines:
    ```
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} displaybootmenu yes
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} timeout 5
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} bootems yes
    bcdedit /store <drive letter>:\boot\bcd /ems {identifier} ON
    bcdedit /store <drive letter>:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
    ```
11. Detach the repaired OS disk from the troubleshooting VM and [swap with the OS disk of the original VM](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap)
12. Ensure the VM is now responding to RDP connectivity.
