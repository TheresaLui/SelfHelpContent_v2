<properties
    pageTitle="Azure Disk Encryption Extension and VM Agent Installation Issue"
    description="Resolve installation issues with VM AGent and Azure Disk Encryption extension on Windows VMs"
    infoBubbleText="Resolve GuestAgent ADE Installation Issue"
	service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS,timbasham"
    ms.author="mnanda,tibasham"
    displayOrder=""
    articleId="GuestAgent-ADE-Install-Issue-Insight"
    diagnosticScenario="Resolve VM Agent and ADE installation Issue"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745,16080"
    cloudEnvironments="public,fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM Deployment Template with Disk Encryption has failed

<!--issueDescription-->
We detected that a recent deployment failure for <!--$vmname-->[vmname]<!--/$vmname--> was due to a known issue. Creation of the VM will succeed but Azure Disk Encryption (ADE) will show a failure.

In this scenario the VM creation will succeed, but the installation of the VM Agent as well as enabling ADE will show as failed. This failure occurs because the ADE installation initiates a reboot that interrupts the VM Agent installation.
<!--/issueDescription-->

## **Recommended Steps**

**Note**: It is recommended to follow the steps below to remediate the issue, before opening a support ticket.

A workaround for this issue is to ensure the VM Agent install to completes, before ADE installation restarts the VM by adding another extension to the template and make the ADE extension depend on the this other extension by using the [dependsOn](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/define-resource-dependency) element. 

### If you are installing any other extensions as part of your deployment
    Add the [dependsOn](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/define-resource-dependency) element to your ADE block and reference any one of these extensions. 

### If you are not installing any other extensions as part of your deployment
    You can use the [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/extensions/custom-script-windows#extension-schema (CSE) with a Hello World type script. 
