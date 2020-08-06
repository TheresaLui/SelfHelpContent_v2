<properties
    pageTitle="Azure Stack Hub Stop and Start"
    description="Stopping and Starting Azure Stack Hub"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32630576"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-operator-stopstart"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub Startup and Shutdown

Most support cases related to start and stop are simply due to the extended time that the operation can take. The recommended steps cover the procedures and what to expect. 

## **Recommended Steps**

1. Verify the power status of the physical node by following the instructions from the OEM who supplied your Azure Stack hardware
1. Get the startup for the Azure Stack Hub startup routine by opening a privileged endpoint session from a machine with network access to the Azure Stack Hub ERCS VMs. From the PEP, run `Get-ActionStatus Start-AzureStack`.

## **Recommended Documents**
* [Azure Stack startup](https://docs.microsoft.com/azure/azure-stack/azure-stack-start-and-stop#start-azure-stack) 
* [Azure Stack shutdown](https://docs.microsoft.com/azure/azure-stack/azure-stack-start-and-stop#stop-azure-stack) 
* [Troubleshoot startup and shutdown](https://docs.microsoft.com/azure-stack/operator/azure-stack-start-and-stop#troubleshoot-startup-and-shutdown-of-azure-stack-hub)

