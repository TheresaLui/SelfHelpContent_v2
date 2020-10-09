<properties
    pageTitle="The VM rebooted to complete Windows Update actions"
    description="The Virtual machine was rebooted due to Windows Update actions."
    infoBubbleText="Windows Updates were installed and the VM automatically rebooted as a result."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="windows-update-reboot"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# The Virtual machine was rebooted due to Windows Update actions
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> rebooted due to Windows Updates being applied. To learn more about this reboot review your System Event log located at "%SystemRoot%\System32\Winevt\Logs\System.evtx" and look for Event ID 1074.
<!--/issueDescription-->

## **Recommended Documents**

* [Windows Shutdown Reason Codes](https://docs.microsoft.com/windows/desktop/shutdown/system-shutdown-reason-codes)
