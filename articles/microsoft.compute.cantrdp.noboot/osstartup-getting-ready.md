<properties
    pageTitle="Getting ready VM boot error"
    description="Virtual machine failed to boot because it is stuck at Getting ready screen"
    infoBubbleText="A boot error 'Getting ready' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="OSStartUp-GETTING_READY"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error - Getting ready

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because it is applying Windows updates, or roles/features.
<!--/issueDescription-->

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the text **Getting ready**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* Please follow the instructions provided in the article [Azure VM shows Getting ready or Getting Windows ready on startup](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-configure-update)
