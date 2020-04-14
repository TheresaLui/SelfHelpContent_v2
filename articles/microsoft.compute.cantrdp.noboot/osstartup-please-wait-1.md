<properties
    pageTitle="VM boot error: Pleast wait"
    description="Virtual machine becomes unresponsive during boot and requests that you please wait."
    infoBubbleText="A boot error occurred your VM with the message 'Please wait'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-PLEASE_WAIT"
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
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows became unresponsive with the message **Please wait**. If you encounter this error message, it could be due to a slow boot scenario, typically from a 3rd party service delaying startup of other services. Alternatively, it may be due to a code defect with profsvc.dll where the Profile Service and the Service Control Manager (SCM) have conflicting locks that prevent their processes from completing. There may also be other causes that can only be determined through a crash dump file analysis.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would Windows stuck with the message **Please wait**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands) to prepare a Repair VM and then use Remote Desktop Connection connect to it.

2. In Windows Administrative Tools, open the Registry Editor tool (or enter `REGEDIT` in command prompt), then do the following to validate that the *CleanupProfile* policy is setup:

	1. Highlight `HKEY_LOCAL_MACHINE`, click **File > Load Hive...**, navigate to `\windows\system32\config` and then open the SYSTEM file.

	2. When you click open and are prompted to enter a name, enter `BROKENSOFTWARE`. You can verify the renaming worked by expanding HKEY_LOCAL_MACHINE and see the extra key you just named.

	3. Open BROKENSOFTWARE and validate that the **CleanupProfile** key exists. If it does then continue with step 2, but if it doesn't then [skip to step 5](#memd).

3. Open an elevated CMD instance and enter the following commands:

		Delete CleanupProfiles key:
		REG DELETE "HKLM\BROKENSOFTWARE\Policies\Microsoft\Windows\System" /v CleanupProfiles /f

		Unload the BROKENSOFTWARE hive:
		REG UNLOAD HKLM\BROKENSOFTWARE


4. **If you are not running Windows Server 2012 R2 skip this step.** In Windows, go to **Settings > Update & Security** and click the **Check for updates** button. Windows update KB3161606 or KB3172614 fixed a defect that could be the culprit. After updating, [use step 5 of the Repair Commands to reassemble the VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) and verify if the changes made have resolved the issue.

5. <a name="memd"></a>Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands) to prepare a new Repair VM and then use Remote Desktop Connection connect to it.

If your VM is still not booting, locate the dump file and submit a support ticket:

1. On the repair VM, go to Windows folder in the attached OS disk. If the driver letter that is assigned to the attached OS disk is `F`, you need to go to `F:\Windows`.

2. Locate the `memory.dmp` file, and then [submit a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) with the memory dump file.

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
