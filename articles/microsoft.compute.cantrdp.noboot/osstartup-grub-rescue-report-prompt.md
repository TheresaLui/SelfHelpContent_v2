<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot waiting at GRUB rescue"
    infoBubbleText="Virtual machine failed to boot waiting at GRUB rescue"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="OSStartUp-GRUB_RESCUE_PROMPT"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="linux"
    productPesIds="15571,15797,16454,16470"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>

# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because it is waiting at GRUB rescue.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. This may help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

Please use the [Linux VM boots to GRUB rescue](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-error) troubleshooting guide to resolve the issue.
