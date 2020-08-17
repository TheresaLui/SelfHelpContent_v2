<properties
    pageTitle="Shutting Down Service: Windows Modules Installer"
    description="Virtual machine failed to shut down and gets hung on the 'Shutting down service: Windows Modules Installer' process."
    infoBubbleText="A shut down error occured with OS stuck on the message 'Shutting down service: Windows Modules Installer'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michaeljbuford"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSShutDown-SHUTTING_DOWN_SERVICE_WINDOWS_MODULES_INSTALLER"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/> 

# Shutting Down Service: Windows Modules Installer

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the shutdown process is performing system maintenance operations and making changes to the system. Changes such as binaries updates, and/or feature changes are critical and shouldn't be interrupted till completion. If the process is stopped, it is very likely the OS will get corrupted. It is possible this process will be stuck for a long time (1 hour or more) in which you need to intervene and deal with the corruption consequences afterwards. Intervening also comes with another complication, in that you may or may not have network and other components, since they may have already been turned off during shut down. This will limited the types of approaches you will do on this case.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Shutting Down Service: Windows Modules Installer**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. [Create a new data disk](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal) or open an existing one in a functioning VM
2. [Download the Procdump tool](https://docs.microsoft.com/sysinternals/downloads/procdump) into the healthy data disk on the functioning VM
3. [Detach the healthy data disk from the healthy VM](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk) and then [attach it to the broken VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)
4. Open an elevated command prompt (run as administrator) and execute the following:

	1. Get the process ID (PID) by entering `tasklist /svc | findstr /i trustedins*`
	2. Get a memory dump sample from the hang process *TrustedInstaller.exe* by entering `procdump.exe -s 5 -n 3 -ma <PID HERE>`. Replace `<PID HERE>` with the PID identified earlier.
	3. Now kill the current process to unlock the shutdown process by entering `taskkill /pid <PID HERE> /t /f`. Replace `<PID HERE>` with the PID identified earlier.

5. Once the OS starts again, check if it boots normally:

	1. If it does, then just ensure the OS consistency is ok
	2. If the check does show corruption, then run the `dism /online /cleanup-image /restorehealth` command as many times as is needed until it becomes corruption free
	
6. If the OS is not starting up, is crashing, or is displaying a boot error, then use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to prepare a new Repair VM and then connect to it using Remote Desktop Connection
7. On the repair VM, go to the Windows folder in the attached OS disk and locate the `memory.dmp` file:

	* If the driver letter that is assigned to the attached OS disk is "F", then you need to go to `F:\Windows`
	* If you are having trouble locating the `memory.dmp` file, you may wish to use [non-maskable interrupt (NMI) calls in serial console](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-windows#use-the-serial-console-for-nmi-calls) instead. You can follow the guide to [generate a crash dump file using NMI calls here](https://docs.microsoft.com/windows/client-management/generate-kernel-or-complete-crash-dump).

8. [Submit a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) with the memory dump file

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
