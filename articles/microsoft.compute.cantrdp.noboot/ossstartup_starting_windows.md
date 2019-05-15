<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because it couldn't finitialize Windows"
    infoBubbleText="A boot error 'Please wait for the Local Session Manager' has been found for your virtual machine. The operating system is corrupted and you'll need to restart your machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    authorAlias="v-jasoan"
    displayOrder=""
    articleId="OSStartUp-STARTING_WINDOWS"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM Boot Error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operation system.

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**
To remediate this problem, we recommend taking the following steps:

1. [Stop the VM and create a snapshot.](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager).

2. <!--/Phase 1-->Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager).

3. <!--/Phase 2 Mitigation--> Verify the OS partition that holds the BCD store for the disk is marked as active.

 a. Open an elevated command prompt and open up ''DISKPART'' tool diskpart.

 b. List the disks on the system, look for added disks, and then proceed to select the new disk.

  1. To list the disk: ''list disk''

  2. To select the disk: ''sel disk 1''

 c. List all the partitions on the disk and then proceed to select the partition you want to check. Typically, System Managed partitions are around 350Mb in size.
  1. To list the partitions: ''list partition''
  2. To select the partition:''sel <PARTITION ID>''

  d. Check the status of the partition to verify that it's Active. ''detail partition''

   1. Check the flag called ''Active'' and if it states that isn’t active, then you can change this flag and activate this partition by running ''active''

   2. To validate the changes where done properly, you can list again the partition settings by running ''detail partition''. Then type ''Exit'' when ready.


   4.  Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition.
       * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
       * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB

     a. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step

         ```
         bcdedit /store [Boot partition]:\boot\bcd /enum
         ```

      b. Repair the Boot Configuration data by running the following command lines. You must replace these placeholders by the actual values:
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

5. <!--/Phase 3--> Run [Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). When it will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
