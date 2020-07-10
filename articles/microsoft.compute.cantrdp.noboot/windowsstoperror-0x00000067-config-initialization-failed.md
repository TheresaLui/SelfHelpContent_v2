<properties
    pageTitle="VM boot error: #0x00000067 Configuration Initialization Failed"
    description="Virtual machine failed to boot and needs to restart due to a missing IMC reference, with the message: 'Config Initialization Failed'."
    infoBubbleText="A message that 'Your PC ran into a problem and needs to restart.' with the error 'CONFIG INITIALIZATION FAILED' or code #0x00000067."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="WindowsStopError-0x00000067-CONFIG_INITIALIZATION_FAILED"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: #0x00000067 Configuration Initialization Failed
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code #0x00000067 'Config Initialization Failed'. This issue occurs when the Initial Machine Configuration (IMC) reference is setup on the Boot loader, but its reference is missing in the registry.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would show the message **Your PC ran into a problem and needs to restart** with the error code **CONFIG INITIALIZATION FAILED** or code **0x00000067**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. <a name="prepvm"><a/>Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to prepare a Repair VM. Once prepared, use Remote Desktop Connection connect to the Repair VM.

2. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is the Boot partition and the Windows partition.

    > The Windows partition contains a folder named "Windows," and this partition is larger than the others.

    > The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the *Hide protected operating system files (Recommended)* option. The boot partition is typically about 300 MB-500 MB in size.

3. Open an elevated command prompt (run as administrator) and gather the current booting setup info using the `bcdedit /store <DRIVE LETTER>:\boot\bcd /enum` command.

    > Replace any `<TEXT HERE>` with the appropriate information indicated.

4. In the Windows Boot Loader information displayed, notice the references **imcdevice** and **imchivename**. You will need to delete those references with the following commands:

        bcdedit /store <DRIVE LETER>:\boot\bcd /deletevalue {<IDENTIFIER>} imcdevice
        bcdedit /store <DRIVE LETER>:\boot\bcd /deletevalue {<IDENTIFIER>} imchivename

    > Replace any `<TEXT HERE>` with the appropriate information indicated.

    > "Boot partition" is the partition that contains a hidden system folder named "Boot".

    > "Identifier" is the identifier of Windows Boot Loader you found in the previous step.

5. Use [step 5 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to reassemble the VM. Once reassembled, test if the VM is responding to RDP connectivity to see if this has fixed the issue.

6. If the issue persists, repeat [step 1 to create a new repair VM and then connect to it](#prepvm). Once the VM is prepared, open an elevated command prompt (run as administrator) and continue with the next steps.

7. Check which ControlSet the machine is booting from. You will see its key number in the `HKLM\BROKENSYSTEM\Select\Current` directory. Once located, just make the changes on the registry keys on that branch. See example below where the disk is drive F:.

        reg load HKLM\BROKENSYSTEM f:\windows\system32\config\SYSTEM
    
        reg query "HKLM\BROKENSYSTEM\Select" /v Current

    > If your disk isn't drive F:, update the letter to match your situation.

8. Run the following commands to create the property *ErrorControlPolicy* on the IMC keys:

    1. Get the current ControlSet from where the OS is booting:

            for /f "tokens=3" %x in ('reg query HKLM\SYSTEM\Select /v Current') do set ControlSet=%x
            set ControlSet=%ControlSet:~2,1%
        
    2. Create the IMC property:

            set key=HKLM\BROKENSYSTEM\ControlSet00%ControlSet%\Control\InitialMachineConfig\_Global
            reg add %key% /v ErrorControlPolicy /t REG_DWORD /d 0 /f
            set key=HKLM\BROKENSYSTEM\ControlSet00%ControlSet%\Control\InitialMachineConfig\System
            reg add %key% /v ErrorControlPolicy /t REG_DWORD /d 0 /f

    3. Unload BROKENSYSTEM:
        
            reg unload HKLM\BROKENSYSTEM

9. Use [step 5 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to reassemble the VM. Once reassembled, test if the VM is responding to RDP connectivity.

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
