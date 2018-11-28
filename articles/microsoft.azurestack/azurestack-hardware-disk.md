<properties
    pageTitle="Azure Stack disks"
    description="Azure Stack Physical Disks"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567931,32629241"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack Disks

## **Recommended steps**

1. When a disk fails, you receive an alert that tells you that connectivity has been lost to a physical disk
2. The alert description contains the scale unit node and the exact physical slot location for the disk that you must replace
2. Follow your OEM hardware vendor’s FRU instructions for physical disk replacement.
3. [Monitor the status of virtual disk repair](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-replace-disk#check-the-status-of-virtual-disk-repair)

**Note:** Actual disk replacement steps will vary based on your original equipment manufacturer (OEM) hardware vendor. See your vendor’s field replaceable unit (FRU) documentation for detailed steps that are specific to your system. 

## **Recommended documents**

[Replace a Physical Disk in Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-replace-disk)