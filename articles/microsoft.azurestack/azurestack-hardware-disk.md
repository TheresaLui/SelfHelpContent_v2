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
    cloudEnvironments="public"
	articleId="f7b38aef-8641-4e65-8a79-b2196bcf88da"
/>

# Azure Stack Disk Failure

## **Recommended Steps**

1. When a physical disk fails in Azure Stack, you will receive an alert that tells you that connectivity has been lost to a physical disk
2. The alert description contains the scale unit node and the exact physical slot location for the disk that you must replace
2. Follow your OEM hardware vendor’s field replacement unit (FRU) documentation for detailed instructions on physical disk replacement
3. Continue to [monitor the status of virtual disk repair](https://docs.microsoft.com/azure/azure-stack/azure-stack-replace-disk#check-the-status-of-virtual-disk-repair) on the privileged endpoint, until virtual disks are healthy

## **Recommended Documents**

* [Replace a Physical Disk in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-replace-disk)
