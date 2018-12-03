<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot with a BitLocker Key prompt"
    infoBubbleText="A boot error 'Plug in the USB drive that has the BitLocker key' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ram-kakani,timbasham"
    authorAlias="ramakk,tibasham"
    displayOrder=""
    articleId="BootError--BITLOCKER"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM boot error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code **Plug in the USB drive that has the BitLocker key**. This issue occurs if retrieval of the BEK files from Azure Key Vault has encountered issues while starting a VM that is using [Azure Disk Encryption extension](https://docs.microsoft.com/azure/security/azure-security-disk-encryption).

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **Plug in the USB drive that has the BitLocker key**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**
To restore the access to the VM please follow the steps in this troubleshooting guide, [BitLocker boot errors on an Azure VM](https://review.docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-bitlocker-boot-error).

