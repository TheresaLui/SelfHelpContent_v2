<properties
    pageTitle="Azure Disk Encryption Extension Installation Issue"
    description="Resolve installation issues with Azure Disk Encryption extension on Azure Windows VMs"
    infoBubbleText="Resolve GuestAgent ADE Installation Issue"
	service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS,timbasham"
    ms.author="mnanda,tibasham"
    displayOrder=""
    articleId="GuestAgent-ADE-Install-Issue-Insight"
    diagnosticScenario="Resolve GuestAgent ADE Installation Issue"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745,16080"
    cloudEnvironments="public,fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM Deployment Template with Disk Encryption has failed

We detected that a recent deployment failure for **<!--$vmname-->[vmname]<!--/$vmname-->** was due to a known issue. Creation of the VM will succeed but Azure Disk Encryption will show a failure.

In this scenario the VM creation will succeed, but the installation of the Azure Guest Agent as well as Azure Disk Encryption will show as failed. This failure occurs because the Azure Disk Encryption installation initiates a reboot interrupting the installation of the Azure Guest Agent.

## **Recommended Steps**

**Note**: It is recommended to follow the steps below to remediate the issue, before opening a support ticket.

??? Why do we need another extension, does ADE extension not respect dependson ???

??? Need to provide an example ???

A workaround for this issue is to give more time for the GuestAgent install to complete, by adding another extension to the template and have the ADE extension depend on the other extension using [dependsOn](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/define-resource-dependency). 

Because other extensions don't have risk of causing a reboot before GuestAgent install completes, this will make sure GuestAgent is installed by the time the template deploys the ADE extension to the VM.
