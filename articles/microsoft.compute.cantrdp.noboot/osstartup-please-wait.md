<properties
    pageTitle="VM boot error: Pleast wait"
    description="Virtual machine becomes unresponsive during boot and requests that you please wait for the Local Session Manager."
    infoBubbleText="A boot error occurred your VM with the message 'Please wait for the Local Session Manager'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-PLEASE-WAIT"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: Please wait

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state. If you encounter this error message, you will need to perform a crash dump file analysis to determine the root cause.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would Windows stuck with the message **Please wait for the Local Session Manager**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands) to prepare a new Repair VM, then use Remote Desktop Connection to connect to it
2. Locate the dump file and submit a support ticket:

    1. On the repair VM, go to Windows folder in the attached OS disk. If the driver letter that is assigned to the attached OS disk is `F`, you need to go to `F:\Windows`.
    2. Locate the `memory.dmp` file, and then [submit a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) with the memory dump file

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
