<properties
    pageTitle="VM boot error:Getting Windows ready"
    description="Virtual machine failed to boot during the 'Getting Windows ready' process."
    infoBubbleText="A boot error occurred where your VM is stuck during boot of the OS, with the message 'Getting Windows ready'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michaeljbuford"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="dc4015dc-fdb8-45d4-8302-2c6568ad53dd"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: Getting Windows ready

<!--issueDescription-->
This article provides steps to resolve issues where the operating system cannot finish booting because it is stuck applying computer settings in an Azure VM.
<!--/issueDescription-->

When you use [Boot diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) to view the screenshot of the VM, you will see that the screenshot displays the operating system deadlocked with message: `Getting Windows ready. Don't turn off your computer`.

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [VM startup is stuck on "Getting Windows ready. Don't turn off your computer"](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-vm-boot-configure-update) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
