<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot due to incorrect generalization"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    displayOrder=""
    articleId="OSStartUp--IMAGE_STATUS_UNDEPLOYABLE"
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
We have investigated and determined that your virtual machine <!--$vmname-->**[vmname]**<!--/$vmname--> is in an inaccessible state because Windows was not properly generalized prior to deployment of the image.  This can happen when a specialized disk is deployed as generalized, or the generalization was not completed.  You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to see the current state of your VM, for this issue the screenshot would reflect that the VM is waiting for license acceptance.<br>
<!--/issueDescription-->

## **Recommended Steps**
To resolve the issue you must rebuild the image and redeploy the VM.  For details on how to do this please refer to [Prepare a Windows VHD or VHDX to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image), and [Create a managed image of a generalized VM in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/capture-image-resource).<br>
