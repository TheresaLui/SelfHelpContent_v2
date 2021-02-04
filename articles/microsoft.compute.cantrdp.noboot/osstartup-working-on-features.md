<properties
    pageTitle="VM not booting with - Working on features"
    description="Virtual machine failed to boot with 'Working on features' on the screen"
    infoBubbleText="The VM is not booting with 'Working on features' on the screen of your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="OSStartUp-WORKING_ON_FEATURES"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM not booting with - 'Working on features'

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with **Working on features** on the screen. If you encounter this, a VM stuck at this message, it means that the OS boot process is trying to add or remove features but may be stalled. 
<!--/issueDescription-->

Use the [**Boot Diagnostics Screenshot**](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot may reflect **Working on features XX% complete Don't turn off your computer**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [VM not booting - Working on features](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/azure-vm-cannot-rdp-working-features) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
