<properties
    pageTitle="Windows Stop Error: #0x000000D1 'DRIVER IRQL NOT LESS OR EQUAL'"
    description="Virtual machine failed to boot with the stop code 'DRIVER IRQL NOT LESS OR EQUAL' and now Windows wants to restart automatically."
    infoBubbleText="A Windows stop code 'DRIVER IRQL NOT LESS OR EQUAL' has been found while booting your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="WindowsStopError-0x000000D1-DRIVER_IRQL_NOT_LESS_OR_EQUAL"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Windows Stop Error: 'DRIVER IRQL NOT LESS OR EQUAL' while booting a VM

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with stop code 'DRIVER IRQL NOT LESS OR EQUAL'. If you encounter this error message, it typically means that Windows encountered a race condition.
<!--/issueDescription-->

To confirm the current state of your VM, refer to the [**Boot Diagnostics Screenshot**](datablade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics). The screenshot should reflect the error code: <br> 
"Your PC ran into a problem and needs to restart. We're just collecting some error info, and then we’ll restart for you. (##% complete) Stop code: DRIVER IRQL NOT LESS OR EQUAL." 

This may help you determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Windows Stop Error #0x000000D1 "DRIVER IRQL NOT LESS OR EQUAL"](https://docs.microsoft.com/troubleshoot/azure/virtual-machines/azure-vm-cannot-rdp-driver-irql-not-less-equal) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
