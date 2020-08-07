<properties  
    pageTitle="My Windows VM is not booting"
    description="My Windows VM is not booting"
    service=""
    resource=""
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675600"
    resourceTags=""
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ec711657-87b8-4556-8a17-bd8172ef7921"
	ownershipId="Compute_VirtualMachines_Content"
/>

# My Windows VM is not booting

4 out of 5 customers resolved their VM boot issue using the steps listed below.<br>

## **Recommended Steps**

**Note**: It is **recommended** to follow the troubleshooting steps below to first identify the problem, then perform the remediation step(s) before opening a support ticket:

### If you cannot connect to your Windows virtual machine (VM) and are unsure of the cause, the following troubleshooting steps should be performed

* Verify that your VM has been started
* If your VM fails to start and you recently applied Windows Updates please see [Troubleshooting VM not booting after Windows Update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)
* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) in Azure

### If your VM is not at the **ctrl-alt-del** screen, it may be experiencing a boot error

1. Restart the virtual machine to address boot issues
2. Review the [common boot errors and solutions for non-bootable VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot) troubleshooting guide

**Common issues associated to specific boot errors:**<br>

* [Updating Boot Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)
* [Check Disk Boot Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-check-disk-boot-error)
* [BitLocker Boot Error](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-bitlocker-boot-error)
* [Boot Configuration Update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-configure-update)
* [Common Blue Screen Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-common-blue-screen-error)
* [Critical Service Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-critical-service-failed-boot-error)
* [Reboot loop](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-reboot-loop)

## **Recommended Documents**

* [Troubleshoot specific Remote Desktop connection errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-specific-rdp-errors)
* [Detailed troubleshooting across network components](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)
* [Address Remote Desktop License Server error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-specific-rdp-errors#rdplicense)
