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
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->. We have identified that your VM is currently in an inaccessible state because Windows is waiting for **user inputs** to complete an ongoing installation/upgrade. The issue occurs when the OS is performing an in-place upgrade on the VM.  This can be detected using the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade).<br>
<!--/issueDescription-->

## **Recommended Steps**
Currently running in-place upgrade on an Azure VM is not supported however it could be mitigated by using a *Nested Hyper-V Environment*
1. Stop de-allocate the Virtual Machine <!--$vmname-->[vmname]<!--/$vmname--> and save a copy of the OS disk, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
2. Complete the setup using the copy of the OS disk in a *Nested Hyper-v Environment*. Please refer to [Troubleshoot a problem Azure VM by using nested virtualization in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/troubleshoot-vm-by-use-nested-virtualization) and complete the setup process for the *in-place upgrade*.
3. Once the disk is fixed, detach the repaired OS disk from the troubleshooting VM. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/os-disk-swap)  