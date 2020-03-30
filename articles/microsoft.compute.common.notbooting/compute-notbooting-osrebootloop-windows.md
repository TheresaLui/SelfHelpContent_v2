<properties  
    pageTitle="My Windows VM is stuck in a reboot loop"
    description="My Windows VM is stuck in a reboot loop"
    service=""
    resource=""
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675601"
    resourceTags=""
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax"
    articleId="923b40ea-1562-4f11-b0ed-513148c31966"
	ownershipId="Compute_VirtualMachines_Content"
/>

# My Windows VM is stuck in a reboot loop

4 out of 5 customers resolved their VM boot issue using the steps listed below.<br>

## **Recommended Steps**

**Note**: It is **recommended** to follow the troubleshooting steps below to first identify the problem, then perform the remediation step(s) before opening a support ticket:

### If you cannot connect to your Windows virtual machine (VM) and are unsure of the cause, the following troubleshooting steps should be performed

* Verify that your VM has been started<br>
* Understand [how to use boot diagnostics to troubleshoot Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) in Azure

### If your VM is not at the **ctrl-alt-del** screen, it may be experiencing a boot error

1. Restart the virtual machine to address boot issues
2. Review the [common boot errors and solutions for non-bootable VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot) troubleshooting guide

**Common issues associated to specific boot errors:**<br>

  * [Reboot loop](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-reboot-loop)<br>
  * [Boot Configuration Update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-configure-update)<br>
  * [Check Disk Boot Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-check-disk-boot-error)<br>
  * [BitLocker Boot Error](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-bitlocker-boot-error)<br>
  * [Common Blue Screen Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-common-blue-screen-error)<br>
  * [Critical Service Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-critical-service-failed-boot-error)<br>
  * [Updating Boot Error](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)
  

## **Recommended Documents**

  * [Troubleshoot specific Remote Desktop connection errors](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#troubleshoot-specific-remote-desktop-connection-errors)<br>
  * [Detailed troubleshooting across network components](https://azure.microsoft.com/documentation/articles/virtual-machines-rdp-detailed-troubleshoot/)<br>
  * [Address Remote Desktop License Server error](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-remote-desktop-connections/#rdplicense)
