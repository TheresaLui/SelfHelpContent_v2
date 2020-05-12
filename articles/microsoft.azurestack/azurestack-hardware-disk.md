<properties
    pageTitle="Azure Stack disks"
    description="Azure Stack Physical Disks"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629241"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="f7b38aef-8641-4e65-8a79-b2196bcf88da"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Disk Failure

## **Recommended Steps**

If a physical disk fails, you should replace it as soon as possible.

Actual disk replacement steps will vary based on your original equipment manufacturer (OEM) hardware vendor. Before contacting Microsoft Customer Support Service, see your vendor's field replaceable unit (FRU) documentation for detailed steps that are specific to your system.

1. When a physical disk fails in Azure Stack, an alert says that connectivity has been lost to a physical disk
2. You can get the scale unit node and physical slot location from the [disk alert information](https://docs.microsoft.com/azure-stack/operator/azure-stack-replace-disk#review-disk-alert-information)
3. Follow your OEM hardware vendor's FRU instructions to [replace the disk](https://docs.microsoft.com/azure-stack/operator/azure-stack-replace-disk#replace-the-disk)

## **Recommended Documents**

* [Check the status of virtual disk repair using Azure Stack Powershell](https://docs.microsoft.com/azure-stack/operator/azure-stack-replace-disk#check-the-status-of-virtual-disk-repair-using-azure-stack-powershell)
* After you replace the disk, [check the status of virtual disk repair using the privileged endpoint](https://docs.microsoft.com/azure-stack/operator/azure-stack-replace-disk#check-the-status-of-virtual-disk-repair-using-the-privileged-endpoint)
* If the virtual disk repair job appears stuck, [troubleshoot virtual disk repair using the privileged endpoint](https://docs.microsoft.com/azure-stack/operator/azure-stack-replace-disk#troubleshoot-virtual-disk-repair-using-the-privileged-endpoint)
