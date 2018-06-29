<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot with error *0xC000000F*"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    displayOrder=""
    articleId="VMCannotRDP-BootError-0xC000000F-BootBCDorWinLoadexe"
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
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->. We have identified that your VM is currently in an inaccessible state because Windows failed to boot with error code **0xC000000F**. This issue occurs when the boot configuration data store (BCD) is corrupt.  This can be detected using the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade).<br>
<!--/issueDescription-->

## **Recommended Steps**
To fix the VM, please follow the troubleshooting steps indicated below:
1. Please make a note of the File name and the path from the screenshot from the Virtual Machine <!--$vmname-->[vmname]<!--/$vmname-->
2. If the File name refers to the file *\Windows\system32\config\SYSTEM* then save a copy of the OS disk, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy).
3. Attach the copy/snapshot of the OS disk of the VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
4. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
5. Open an elevated Command Prompt (**CMD, run as Administrator**), and run the following command for the drive you attached:
    ```
    bcdedit /store <drive letter>:\boot\bcd /enum
    ``` 
6. Record the identifier of the **Windows Boot Loader** this will have **\Windows\system32\winload.exe** as the value for the path property.  
7. Run the following commands using the attached drive's **drive letter**, and the **identifier** from the above step.
    ```
    bcdedit /store <drive letter>:\boot\bcd /set {identifier} device partition=<drive letter>:
    bcdedit /store <drive letter>:\boot\bcd /set {identifier} integrityservices enable
    bcdedit /store <drive letter>:\boot\bcd /set {identifier} recoveryenabled Off
    bcdedit /store <drive letter>:\boot\bcd /set {identifier} osdevice partition=<drive letter>:
    bcdedit /store <drive letter>:\boot\bcd /set {identifier} bootstatuspolicy IgnoreAllFailures
    ```
8. If desired now is a good time to enable your Windows VM to use Azure Serial Console which can help in diagnosing and resolving future issues. [Virtual machine serial console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)
10. Using the **drive letter**, **identifier**, and elevated Command Prompt from above run the following commands:
    ```
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} displaybootmenu yes
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} timeout 5
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} bootems yes
    bcdedit /store <drive letter>:\boot\bcd /ems {identifier} ON
    bcdedit /store <drive letter>:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
    ```
11. Detach the repaired OS disk from the troubleshooting VM. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/os-disk-swap)