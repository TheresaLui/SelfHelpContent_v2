<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to respond to RDP as Windows Updates installation is in progress"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_UPDATE_INSTALLATION"
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

We have investigated and identified that your VM is currently in an inaccessible state because a Windows Update installation is in progress. The issue occurs when a there are a high number of pending updates to be installed.<br>

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause. .<br>
<!--/issueDescription-->

## **Recommended Steps**
Windows Update installation can take some time depending on the number and size of the updates being installed. Allow the VM to go through the process without interruption. If the VM is in this state for several hours, attempt to restart the VM from the Azure portal.

If the issue persists, follow the mitigation steps below to recover the VM:

1. Stop/de-allocate the VM and save a copy of the OS disk or create a snapshot. Follow the step in the article [Create a copy or snapshot of the OS disk of an Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized#option-3-copy-an-existing-azure-vm).
2. Attach the copy/snapshot of the OS disk as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal).
3. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
4. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition.

   * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
   * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB.
6. Ensure there is a 'temp' folder in C:\ drive by executing `C:\dir`, else create one using `C:\md temp`.
7. Using [DISM](https://docs.microsoft.com/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows) query the updates that are currently installed and pending installation:

    ```
    dism /image:<drive letter>:\ /get-packages > c:\temp\Patch_level.txt
    ```

7. Open the file c:\temp\Patch_level.txt and read it starting from the bottom to the top. The Windows Update impacting the virtual machine will be listed with the status **Install Pending** or **Uninstall Pending**.
8. Remove the problematic Windows Updates by performing the following commands for each of the Windows Updates that are in status **Install Pending / Uninstall Pending**.

    ```
    dism /Image:<drive letter>:\ /Remove-Package /PackageName:<package to be removed>
    ```

9. Detach the repaired OS disk from the troubleshooting VM. [Then, swap the OS disk with the original VM](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap)
10. Start the VM and verify if you are able to connect via RDP.
