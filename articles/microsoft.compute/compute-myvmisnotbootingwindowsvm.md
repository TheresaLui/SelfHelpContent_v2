<properties
    pageTitle="Resolve a not booting issue with your Windows VM"
    description="Resolve a not booting issue with your Windows VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds="32675597,32675600,32675601,32675599"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fbb1ecda-19a5-40a0-89e0-145c5076c8c0"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolve connection issue with your Windows VM

4 out of 5 customers resolved their VM not booting issue using the steps listed below.<br>

## **Recommended Steps**

**Note**: It is **recommended** to follow the troubleshooting steps below to first identify the problem, then perform the remediation step(s) before opening a support ticket.

If your Windows virtual machine (VM) is not booting and you are unsure of the cause, you can start by accessing the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) for your VM and determine if the VM is experiencing a boot error.

* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) in Azure<br>
* Verify that [Boot Diagnostics](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) are enabled for your VM<br>
* View the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) before continuing to the next section

### If your VM is not at the ctrl-alt-del screen, it may be experiencing a boot error

1. Restart the virtual machine to address boot issues by clicking **Restart** at the top of the [VM resource blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId)<br>
2. Review the [common boot errors and solutions for non-bootable VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot) troubleshooting guide

**Common issues associated to specific boot errors:**<br>

  * [Check Disk Boot Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-check-disk-boot-error)<br>
  * [BitLocker Boot Error](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-bitlocker-boot-error)<br>
  * [Boot Configuration Update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-configure-update)<br>
  * [Common Blue Screen Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-common-blue-screen-error)<br>
  * [Critical Service Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-critical-service-failed-boot-error)<br>
  * [Updating Boot Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)<br>
  * [Reboot loop](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-reboot-loop)

## **Recommended Documents**

* [Review the RDP troubleshooting guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)<br>
* Access the [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM and verify it is running.
