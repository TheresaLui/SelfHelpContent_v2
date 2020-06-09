<properties
    pageTitle="Resolve a not booting issue with your Windows VM"
    description="Resolve a not booting issue with your Windows VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder="34"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows, windowsSQL"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="compute-myvmisnotbootingwindowsvm-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# Resolve connection issue with your Windows VM

4 out of 5 customers resolved their VM not booting issue using the steps listed below.

## **Recommended Steps**

**Note**: It is **recommended** to follow the troubleshooting steps below to first identify the problem, then perform the remediation step(s) before opening a support ticket.

If your Windows virtual machine (VM) is not booting and you are unsure of the cause, you can start by accessing the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) for your VM and determine if the VM is experiencing a boot error.

* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.azure.cn/virtual-machines/troubleshooting/boot-diagnostics) in Azure
* Verify that [Boot Diagnostics](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) are enabled for your VM
* View the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) before continuing to the next section

### If your VM is not at the ctrl-alt-del screen, it may be experiencing a boot error

1. Restart the virtual machine to address boot issues by clicking **Restart** at the top of the [VM resource blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId)
2. Review the [common boot errors and solutions for non-bootable VMs](https://docs.azure.cn/virtual-machines/troubleshooting/boot-error-troubleshoot) troubleshooting guide

**Common issues associated to specific boot errors:**

* [Check Disk Boot Error](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-check-disk-boot-error)
* [BitLocker Boot Error](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-bitlocker-boot-error)
* [Boot Configuration Update](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-vm-boot-configure-update)
* [Common Blue Screen Error](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-common-blue-screen-error)
* [Critical Service Failure](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-critical-service-failed-boot-error)
* [Updating Boot Error](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)
* [Reboot loop](https://docs.azure.cn/virtual-machines/troubleshooting/troubleshoot-reboot-loop)

## **Recommended Documents**

* [Review the RDP troubleshooting guide](https://docs.azure.cn/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)
* Access the [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM and verify it is running.
