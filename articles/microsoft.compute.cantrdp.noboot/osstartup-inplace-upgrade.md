<properties
    pageTitle="VM boot error"
    description="Virtual machine failed as it is expecting *user inputs* on the console screen"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    displayOrder=""
    articleId="OSStartUp-INPLACE_UPGRADE"
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
We have investigated and determined that your virtual machine <!--$vmname-->**[vmname]**<!--/$vmname--> is in an inaccessible state because Windows is waiting for **user inputs** to complete an ongoing installation/upgrade. The issue occurs when the OS is performing an in-place upgrade on the VM.  You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to see the current state of your VM.  For this issue, the screenshot would reflect that the VM is waiting for setup to be completed.<br>
<!--/issueDescription-->

## **Recommended Steps**
Currently running in-place upgrade on an Azure VM is not supported.  However, it can be performed by using a *Nested Hyper-V Environment*.  The following steps walk you through how to do this.
1. Stop/deallocate the Virtual Machine <!--$vmname-->[vmname]<!--/$vmname--> and save a copy of the OS disk.  (See [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy))
2. Complete the setup using the copy of the OS disk in a *Nested Hyper-v Environment*. Please refer to [Troubleshoot a problem Azure VM by using nested virtualization in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/troubleshoot-vm-by-use-nested-virtualization) and complete the setup process for the *in-place upgrade*.
3. Once the disk is fixed, detach the repaired OS disk from the troubleshooting VM that was created in step 2. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/os-disk-swap). 
