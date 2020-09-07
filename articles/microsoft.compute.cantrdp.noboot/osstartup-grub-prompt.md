<properties
    pageTitle="Linux VM boots to Grub Rescue"
    description="Your Linux Virtual Machine has failed to boot and is currently in Grub Rescue."
    infoBubbleText="Your Linux Virtual Machine has failed to boot and is currently in Grub Rescue."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="OSStartUp-GRUB_PROMPT"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="linux"
    productPesIds="15571,15797,16454,16470"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>

# VM Boot Error - Grub Rescue

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because has entered Grub Rescue.
<!--/issueDescription-->

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the text **grub rescue**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* Please follow the instructions provided in the article [Linux VM boots to Grub Rescue](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-error)
