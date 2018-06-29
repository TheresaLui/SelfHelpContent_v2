<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to process Windows Updates during installation"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_UPDATE_ROLLBACK"
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
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->. We have identified that your VM is currently in an inaccessible state because Windows failed to install one or more Windows Updates with error code **Failure configuring Windows updates - Reverting changes**. The issue occurs when a there are a high number of pending updates to be installed or one of the updates has become corrupt.  This can be detected using the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade).<br>
<!--/issueDescription-->

## **Recommended Steps**
Depending on the number of updates that are installing or going through rollback, this could take some time. Do not interrupt this process, leave the VM in place until the OS recovers itself.  However if after 8 hours the VM is still in this state, restart the VM from the Azure portal.

If the issue continues even after a restart please follow the mitigation below:

1. Stop/de-allocate the VM and save a copy of the OS disk or create a snapshot, see [Create a copy or snapshot of the OS disk of an Azure VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm) .
2. Attach the copy/snapshot of the OS disk as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal)
3. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
4. Identify the boot partition and the Windows partition. If there is only one partition on the OS disk, this partition is the Boot partition and the Windows partition.
    *  The Windows partition contains a folder named **Windows**, and this partition is typically larger than the others.
6. Using DISM query the updates that are currently installed and pending installation:
    ```
    dism /image:<drive letter>:\ /get-packages > c:\temp\Patch_level.txt
    ```
7. Open the file c:\temp\Patch_level.txt and read it starting from the bottom to the top, the Windows Update impacting the Virtual Machine will be listed with the status **Install Pending** or **Uninstall Pending**.
8. Remove the problematic Windows Updates by performing the following commands for each of the Windows Updates that are in status **Install Pending / Uninstall Pending**.
    ```
    dism /Image:<drive letter>:\ /Remove-Package /PackageName:<package to be removed>
    ```    
9. Detach the repaired OS disk from the troubleshooting VM. [Then, swap the OS disk with the original VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/os-disk-swap)
10. Start the VM and verify if you are able to connect via RDP.  