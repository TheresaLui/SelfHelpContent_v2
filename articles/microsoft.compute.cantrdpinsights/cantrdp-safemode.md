<properties
    pageTitle="VM boot error"
    description="Virtual machine was started in Safe Mode"
    infoBubbleText="We have detected that your VM was started in safe mode. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ram-kakani,timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="cantrdp-safemode"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Virtual machine was started in Safe Mode

<!--issueDescription-->
We have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state because it started in Safe Mode.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**

* To restart the VM in normal mode, please try the below steps using the [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/serialConsole)
* If you’re unfamiliar with the serial console or would like additional information, please refer to our [user guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)

##### From the Serial Console:

* Query the boot configuration data `bcdedit /enum`
* The Windows Boot Loader section will show an additional option 'safeboot' indicating its either 'Minimal' or 'Networking' similar to the below output:

  ```
  C:\Users\Administrator>bcdedit /enum

  Windows Boot Manager
  --------------------
  identifier              {bootmgr}
  device                  unknown
  description             Windows Boot Manager
  locale                  en-US
  inherit                 {globalsettings}
  bootshutdowndisabled    Yes
  default                 {current}
  resumeobject            {cf002dae-31db-11e8-a8f2-e41d2d742d41}
  displayorder            {current}
  toolsdisplayorder       {memdiag}
  timeout                 30

  Windows Boot Loader
  -------------------
  identifier              {current}
  device                  boot
  path                    \Windows\system32\winload.exe
  description             Windows Server 2016
  locale                  en-US
  inherit                 {bootloadersettings}
  recoverysequence        {f6cb6190-31dc-11e8-a93c-00155de6cd26}
  recoveryenabled         No
  allowedinmemorysettings 0x15000075
  osdevice                boot
  systemroot              \Windows
  resumeobject            {cf002dae-31db-11e8-a8f2-e41d2d742d41}
  nx                      OptOut
  safeboot                Minimal
  bootstatuspolicy        IgnoreAllFailures
  ems                     Yes
  ```

* Remove the flag "safeboot" from this partition by executing `bcdedit /deletevalue {current} safeboot`
* Exit from the Serial Console and Restart the VM
* Verify if you are able to connect via RDP
