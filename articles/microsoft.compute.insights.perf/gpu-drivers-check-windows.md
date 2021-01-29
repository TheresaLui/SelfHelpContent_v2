<properties
    pageTitle="Update GPU Drivers"
    description="GPU Drivers not installed or outdated"
    infoBubbleText="GPU Drivers not installed or outdated"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS"
    ms.author="mnanda"
    displayOrder=""
    articleId="MissingGPUDriversOnNSeriesVM-Windows"
    diagnosticScenario="GPU Drivers not installed or outdated"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="windows,windowsSQL"
    productPesIds="14749,14745"
    cloudEnvironments="public,fairfax,usnat,ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Missing or outdated GPU Drivers on N-Series VM can impact Performance

<!--issueDescription-->
The GPU may not be visible due to missing GPU drivers, or GPU performance could be reduced due to outdated GPU drivers. We strongly recommend verifying that the GPU drivers on the VM  **<!--$vmname-->[vmname]<!--/$vmname-->** are installed and updated to the latest build.
<!--/issueDescription-->

## **Recommended Steps**
For the VM **<!--$vmname-->[vmname]<!--/$vmname-->**, you may leverage the applicable GPU installation link, based on the VM Series.
* NC, NCv2, NCv3, ND, NDv2, NV, and NVv3 series VMs use [NVIDIA drivers](https://docs.microsoft.com/azure/virtual-machines/windows/n-series-driver-setup) 
* NVv4 series VMs use [AMD drivers](https://docs.microsoft.com/azure/virtual-machines/windows/n-series-amd-driver-setup)
