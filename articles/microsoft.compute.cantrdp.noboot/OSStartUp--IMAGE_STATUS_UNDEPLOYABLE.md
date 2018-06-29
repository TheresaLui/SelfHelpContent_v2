<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot due to incorrect generalization"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="Timothy Basham"
    displayOrder=""
    articleId="OSStartUp--IMAGE_STATUS_UNDEPLOYABLE"
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
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->. We have identified that your VM is currently in an inaccessible state because Windows was not properly generalized prior to deployment of the image.  This can happen when a specialized disk is deployed as generalized, or the gerneralization was not completed.  This can be detected using the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade).<br>
<!--/issueDescription-->

## **Recommended Steps**
To resolve the issue you must rebuild the image, for assistance please review [Prepare a Windows VHD or VHDX to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image), and [Create a managed image of a generalized VM in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/capture-image-resource).<br> 
<br>
The following steps can be used to confirm the image state, this is optional.<br>
1. Stop/de-allocate the Virtual Machine <!--$vmname-->[vmname]<!--/$vmname--> and save a copy of the OS disk, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
2. Attach the copy/snapshot of the OS disk of the VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
3. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
3. Open **Regedit.exe**.
3. Click on **HKEY_LOCAL_MACHINE** and from the **File** menu select **Load Hive...**.
3. Browse to the the file **<drive letter>:\Windows\system32\config\SOFTWARE**, where **drive letter** is from the attached disk.
3. When prompted for a name, use **BROKENSOFTWARE**.
3. Check the value of the ImageState key **HKEY_LOCAL_MACHINE\BROKENSOFTWARE\Microsoft\Windows\CurrentVersion\Setup\State\ImageState** it should read **IMAGE_STATE_UNDEPLOYABLE**, this confirms that generalization was not completed.
3. You can now detach the OS disk from the troubleshooting VM. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/os-disk-swap)
