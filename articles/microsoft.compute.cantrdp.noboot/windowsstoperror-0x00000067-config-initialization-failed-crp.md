<properties
pageTitle="VM boot error"
description="Virtual machine failed to boot with known boot error 0x00000067"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="windowsstoperror-0x00000067-config-initialization-failed-crp"
diagnosticScenario="booterror"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# VM boot error
<!--issueDescription-->
## **Boot error found for your virtual machine**
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state because windows failed to boot with error code **0x00000067**. This issue occurs when the Initial Machine Configuration (IMC) reference is set up on the boot loader but its reference is missing in the registry.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To recover the VM and restore connectivity, please follow the troubleshooting steps indicated below:

1. Launch [Azure Cloud Shell](https://shell.azure.com) and select PowerShell (Linux) when you see 'Welcome to Azure Cloud Shell'.
2. If you then see 'You have no storage mounted', select the subscription where the VM you are troubleshooting resides, then select 'Create storage'.
3. From the 'PS Azure:/>' prompt type 'cd /' then <ENTER>.
4. Run the following command to download the scripts. Git is preinstalled in Cloud Shell. You do not need to install it separately.
      ```
      git clone https://github.com/Azure/azure-support-scripts $home/CloudDrive/azure-support-scripts
      ```
5. Switch into the folder by running:
      ```
      cd $home/CloudDrive/azure-support-scripts/VMRecovery/Resource Manager
      ```
6. Run the command <!--$createrescuevm-->[createrescuevm]<!--/$createrescuevm--> to create a new "rescue VM" and attach the OS disk of the problem VM to the rescue VM as a data disk.   
7. Connect to the rescue VM to ensure the newly attached OS disk is online and has a drive letter assigned.
8. Identify the boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is the boot partition and the Windows partition.

  * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
  * The boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB
9. Run the following command line as an administrator to gather the BCD store information.

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
10. Remove the Initial Machine Configuration (IMC) references in the BCD store by executing the below commands. You must replace these placeholders by the actual values:

  * "Boot partition" is the partition that contains a hidden system folder named "Boot."
  * "Identifier" is the identifier of Windows Boot Loader you found in the previous step.

      ```          
      bcdedit /store [Boot partition]:\boot\bcd /deletevalue {[Identifier]} imcdevice
      bcdedit /store [Boot partition]:\boot\bcd /deletevalue {[Identifier]} imchivename
      ```
11. If desired, now is a good time to enable your Windows VM to use [Azure Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console) which can help in diagnosing and resolving future issues. Otherwise, skip to the step 14 to restore the VM.
12. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step

      ```
      bcdedit /store [Boot partition]:\boot\bcd /enum
      ```
13. Enable Azure Serial Console by running the following command lines:

    ```
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} displaybootmenu yes
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} timeout 5
    bcdedit /store <drive letter>:\boot\bcd /set {bootmgr} bootems yes
    bcdedit /store <drive letter>:\boot\bcd /ems {identifier} ON
    bcdedit /store <drive letter>:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
    ```
14. To restore the VM from the OS disk attached to the rescue VM, run <!--$restorevm-->[restorevm]<!--/$restorevm--> script
15. Ensure the VM is now responding to RDP connectivity.
