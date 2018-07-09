<properties
pageTitle="VM boot error"
description="Virtual machine is in the process of applying the configuration changes to Windows"
infoBubbleText="The OS is applying some recent configuration changes and hence the VM is responding to RDP yet. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="OSStartUp-GETTING_WINDOWS_READY"
diagnosticScenario="booterror"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# VM boot error
<!--issueDescription-->
## **Boot error found for your virtual machine**
We have investigated and identified that your VM is currently in an inaccessible state because Windows OS is at **Getting Windows Ready** state. This occurs when there was a configuration change applied via Windows Update or Windows roles/features and the OS is attempting to apply the changes upon the following boot.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
Windows Update installation can take time depending on the number or size of the updates being installed. Allow the VM to go through the process without interruption.

* If the VM is in this state for several hours, attempt to restart the VM from the Azure portal.
* Ensure the VM has booted up via the Boot Diagnostics screenshot.
* Validate if you are able to connect to the VM via RDP.<br>

If the issue persists, a memory dump needs to be collected to continue troubleshooting. If this is the case for you, please email us with your approval to collect a memory dump of this VM and we will investigate further.
