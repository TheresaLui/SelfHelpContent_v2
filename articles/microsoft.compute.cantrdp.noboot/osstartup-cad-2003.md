<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because of a 'Please wait for the Local Session Manager' error."
    infoBubbleText="A boot error 'Please wait for the Local Session Manager' Try disconnecting any drivers that doesn't contain an operating system. Press Ctrl+Alt+Del to restart' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    authorAlias="v-jasoan"
    displayOrder=""
    articleId="OSStartUp-CAD-2003"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM Boot Error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operation system.

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**
To remediate this problem, we recommend taking the following steps:

1. S[Stop the VM and create a snapshot.](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager).

2. <!--/Phase 1-->Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager).

3. <!--/Phase 2 Mitigation--> The OS needs to be reinstalled.

 a.	For Windows Server 2012/Windows 8 and up:

    1.	The settings which comes on the gallery image, are already set to collect a Kernel memory dump in case of an OS crash so you can just proceed with the steps below to cause the interruption.

    2. If a Full memory dump is required then, the following settings are needed:

    ```
    REG ADD "HKLM\SYSTEM\CurrentControlSet\Control\CrashControl" /v CrashDumpEnabled /t REG_DWORD /d 1 /f
    REG ADD "HKLM\SYSTEM\CurrentControlSet\Control\CrashControl" /v DumpFile /t REG_EXPAND_SZ /d "%SystemRoot%\MEMORY.DMP" /f
    ```

    Note: For big machines and to ensure you don't end up in a capacity issue on the C drive, change the key name DumpFile above to create the file in any other drive that has enough space to hold a file as big as the ram memory of the VM

  b. For Windows Server 2008 R2 and Windows 7 VMs you will need as an extra to the above the NMI key:

  ```
  REG ADD "HKLM\SYSTEM\CurrentControlSet\Control\CrashControl" /v CrashDumpEnabled /t REG_DWORD /d 1 /f
  REG ADD "HKLM\SYSTEM\CurrentControlSet\Control\CrashControl" /v DumpFile /t REG_EXPAND_SZ /d "%SystemRoot%\MEMORY.DMP" /f
  ```

  Note: For big machines and to ensure you don't end up in a capacity issue on the C drive, change the key name DumpFile above to create the file in any other drive that has enough space to hold a file as big as the ram memory of the VM.

4.	When the problem is happening then, you can use the portal to send this interruption:

   a.	From the serial console feature menu, select the keyboard option on the menu bar.

   b. Select the Send Non-Maskable Interrupt (NMI) option from the menu.

   c. To validate if the memory dump is happening, you will have the following options:

     1. If EMS service is enabled on the Guest OS (Serial Console Feature prerequirement), then you will have the memory dump collection.

     2. ii.	However if EMS is not enabled on the Guest OS or if this is a Windows client OS Version, then you can check the Boot Diagnostic option and you will see that the VM was crashed with the stop error NMI_HARDWARE_FAILURE.

5. <!--/Phase 3--> Run [Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). When it will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
