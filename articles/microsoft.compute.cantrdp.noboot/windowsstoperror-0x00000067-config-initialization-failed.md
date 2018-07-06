<properties
pageTitle="VM boot error"
description="Virtual machine failed to boot with known boot error 0x00000067"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="WindowsStopError-0x00000067-CONFIG_INITIALIZATION_FAILED"
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
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state because windows failed to boot with error code **0x00000067**. This issue occurs when the Initial Machine Configuration (IMC) reference is setup on the Boot loader but its reference is missing in the registry.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To recover the VM and restore connectivity, please follow the troubleshooting steps indicated below:
1. Stop/deallocate the VM and save a copy of the OS disk or create a snapshot. Please follow the steps at [Create a copy or snapshot of the OS disk of an Azure VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm).
2. Attach the copy/snapshot of the OS disk of the VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
3. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
4. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is the Boot partition and the Windows partition.
  * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
  * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB
5. Run the following command line as an administrator to gather the BCD store information.

      ```
      c:\> bcdedit /store <drive letter>:\boot\bcd /enum

      Windows Boot Manager
      --------------------
      identifier              {bootmgr}
      device                  unknown
      description             Windows Boot Manager
      locale                  en-us
      inherit                 {globalsettings}
      displayorder            {current}
      toolsdisplayorder       {memdiag}
      timeout                 30

      Windows Boot Loader
      -------------------
      identifier              {<<IDENTIFIER>>}
      device                  boot
      path                    \Windows\system32\winload.exe
      description             Windows Server 2016
      locale                  en-US
      inherit                 {bootloadersettings}
      recoverysequence        {821346ba-615b-11e7-a81b-000d3a23c6df}
      recoveryenabled         No
      osdevice                boot
      imcdevice               locate=\IMC.hiv
      systemroot              \Windows
      imchivename             \IMC.hiv
      resumeobject            {e6df4561-50ce-11e7-a810-806e6f6e6963}
      nx                      OptOut
      bootstatuspolicy        IgnoreAllFailures
      ```
6. Remove the Initial Machine Configuration (IMC) references in the BCD store by executing the below commands. You must replace these placeholders by the actual values:
  * "Boot partition" is the partition that contains a hidden system folder named "Boot."
  * "Identifier" is the identifier of Windows Boot Loader you found in the previous step.

      ```          
      bcdedit /store [Boot partition]:\boot\bcd /deletevalue {[Identifier]} imcdevice
      bcdedit /store [Boot partition]:\boot\bcd /deletevalue {[Identifier]} imchivename
      ```
7. If desired now is a good time to enable your Windows VM to use [Azure Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console) which can help in diagnosing and resolving future issues. Otherwise, skip to the step 10 to restore the VM.
8. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step
      ```
      bcdedit /store [Boot partition]:\boot\bcd /enum
      ```
9. Enable Azure Serial Console by running the following command lines:
    ```
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} displaybootmenu yes
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} timeout 5
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} bootems yes
    bcdedit /store <drive letter>:\boot\bcd /ems {identifier} ON
    bcdedit /store <drive letter>:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
    ```
10. Detach the repaired OS disk from the troubleshooting VM. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap)
11. Ensure the VM is now responding to RDP connectivity.
