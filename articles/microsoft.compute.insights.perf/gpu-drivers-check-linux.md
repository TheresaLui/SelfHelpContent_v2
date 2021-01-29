<properties
    pageTitle="Update GPU Drivers"
    description="GPU Drivers not installed or outdated"
    infoBubbleText="GPU Drivers not installed or outdated"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS"
    ms.author="mnanda"
    displayOrder=""
    articleId="MissingGPUDriversOnNSeriesVM-Linux"
    diagnosticScenario="GPU Drivers not installed or outdated"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="linux,redhat,ubuntu"
    productPesIds="16342,15571,15797,16454,16470"
    cloudEnvironments="public,fairfax,usnat,ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Missing or outdated GPU Drivers on N-Series VM can impact Performance

<!--issueDescription-->
The GPU may not be visible due to missing GPU drivers, or GPU performance could be reduced due to outdated GPU drivers. We strongly recommend verifying that the GPU drivers on the VM  **<!--$vmname-->[vmname]<!--/$vmname-->** are installed and updated to the latest build.
<!--/issueDescription-->

## **Recommended Steps**
For the VM **<!--$vmname-->[vmname]<!--/$vmname-->**, please follow the instructions to [install GPU Drivers](https://docs.microsoft.com/azure/virtual-machines/linux/n-series-driver-setup) for Linux.
