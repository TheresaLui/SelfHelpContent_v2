<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because the CHKDSK is in progress."
    infoBubbleText="The CHKDSK is currently in progress. Please allow the process to complete."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="BootError-CHKDSK"
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
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operating system.
<!--/issueDescription-->

## **Recommended Steps**

* Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

* If CHKDSK is in progress, wait for the CHKDSK to complete. The machine will reboot. 
* If CHKDSK is complete but begins again after the machine restarts, it is stuck in a CHKDSK boot loop. You will need to delete the VM, mount the OS disk to a recovery machine, and manually run check disk against that drive: 

```
chkdsk /f <<drive to check>>

Chkdsk reference
The options and switches for Check Disk are used as follows: 
/F Fixes errors on the disk 
/V Displays the full path and name of every file on the disk (FAT16 and FAT32); displays cleanup messages if any (NTFS) 
/R Locates bad sectors and recovers readable information (implies /F) 
/X Forces the volume to dismount first if necessary (implies /F) 
/I Performs a minimum check of index entries (NTFS only) 
/C Skips checking of cycles within the folder structure (NTFS only) 
/L Size Sets the log file size (NTFS only) 
/B Re-evaluates bad clusters on the volume (NTFS only; implies /R)
```
