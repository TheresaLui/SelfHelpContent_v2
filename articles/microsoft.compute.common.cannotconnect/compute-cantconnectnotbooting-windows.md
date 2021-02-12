<properties  
    pageTitle="My Windows VM is not booting for reconnection"
    description="My Windows VM is not booting for reconnection"
    service=""
    resource=""
    authors="scotro,timbasham"
    ms.author="scotro,tibasham"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615532,32628284"
    resourceTags=""
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f77c4d7d-6738-46fb-afea-07b627a597b6"
	ownershipId="Compute_VirtualMachines_Content"
/>

# My Windows VM is not booting for reconnection

4 out of 5 customers resolved their VM boot issue using the steps listed below.<br>

## **Recommended Steps**

**Note**: It is **recommended** to follow the troubleshooting steps below to first identify the problem, then perform the remediation step(s) before opening a support ticket:

### If you cannot connect to your Windows virtual machine (VM) and are unsure of the cause, the following troubleshooting steps should be performed

* Verify that your VM has been started by clicking **Start** at the top of the [VM Resource Blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId)<br>
* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) in Azure
* Verify that [Boot Diagnostics](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) are enabled for your VM
* View the [Boot Diagnostics Blade](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) screenshot before continuing to the next section

### If your VM is not at the **ctrl-alt-del** screen, it may be experiencing a boot error

1. Restart the virtual machine to address boot issues by clicking **Restart** at the top of the [VM Resource Blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId)<br>
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

  * [Troubleshoot specific Remote Desktop connection errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-specific-rdp-errors)<br>
  * [Detailed troubleshooting across network components](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)<br>
  * [Address Remote Desktop License Server error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-specific-rdp-errors#rdplicense)
