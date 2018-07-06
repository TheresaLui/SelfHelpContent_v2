<properties
pageTitle="VM boot error"
description="Virtual machine failed as it is expecting 'user inputs' on the console screen"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="OSStartUp-OOBE"
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
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state due to windows failing to boot and the OS is waiting for user inputs on the screen. This issue occurs due to an incorrect or unsuccessful attempt to generalize the VM via Sysprep.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**

Sysprep prepares the VM to be used as an image by removing all your personal and account information from the virtual machine. For details about Sysprep, see [How to Use Sysprep: An Introduction.](http://technet.microsoft.com/library/bb457073.aspx)<br>
Once a Sysprep has been run on a VM, it is considered generalized and it is irreversible. To restore the virtual machine, follow the steps below:

1. Delete the VM selecting the 'Keep the disks' option.<br>
2. Navigate to the image in the "Images" section in the portal to find the image that was created as a result of the prior capture operation.
3. Create the VM from that image following the steps at [Create a VM from a managed  image.](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)
4. Connect to the VM via RDP to see if the issue is resolved.
5. If the VM still fails to boot with the same error, save a copy of the OS disk. This will help in case of a rollback for recovery. Follow the steps in the article [Create a copy of a specialized Windows VM running in Azure.](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)
6. Now [create a nested virtualization environment](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-vm-by-use-nested-virtualization) to mount the OS disk snapshot to complete the user settings and proceed with the next steps as guided by the Sysprep wizard.
7. Ensure the VM is up and is responding to RDP.
8. If desired, now is a good time to enable your Windows VM to use [Azure Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console) which can help in diagnosing and resolving future issues. Otherwise, skip to the step 12 to restore the VM.
9. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step

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

11. Detach the OS disk snapshot from the rescue VM and [swap with the OS disk of the original VM.](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap)
12. Ensure the VM is now responding to RDP connectivity.
