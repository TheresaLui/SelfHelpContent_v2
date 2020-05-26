<properties
    pageTitle="VM boot error: Applying Registry Policy"
    description="Virtual machine failed to boot due to an error occuring during the 'Applying Registry policy' process."
    infoBubbleText="Windows becomes unresponsive during boot during the 'Applying Registry policy' process."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-APPLYING_REGISTRY_POLICY"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Applying Registry Policy
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because of an unknown error that occurred while the OS was applying the registry policy during boot. A memory dump analysis will need to be performed to find the root cause of the issue.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Applying Registry policy**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to prepare a new Repair VM, then connect to it using Remote Desktop Connection

2. On the repair VM, go to the Windows folder in the attached OS disk and locate the `memory.dmp` file

	* If the driver letter that is assigned to the attached OS disk is "F", then you need to go to `F:\Windows`
	* If you are having trouble locating the `memory.dmp` file, you may wish to use [non-maskable interrupt (NMI) calls in serial console](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-windows#use-the-serial-console-for-nmi-calls) instead. You can follow the guide to [generate a crash dump file using NMI calls here](https://docs.microsoft.com/windows/client-management/generate-kernel-or-complete-crash-dump).

3. [Submit a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) with the memory dump file

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
