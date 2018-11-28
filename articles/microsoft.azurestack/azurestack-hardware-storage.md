<properties
    pageTitle="Azure Stack storage devices"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567943,32629224"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack storage devices
The hyper-converged configuration of Azure Stack allows for the sharing of physical storage devices. The three main divisions of the available storage are between the infrastructure, temporary storage of the tenant virtual machines, and the storage backing the blobs, tables, and queues of the Azure Consistent Storage (ACS) services.<br>

There is storage capacity used for the operating system, local logging, dumps, and other temporary infrastructure storage needs. This local storage capacity is separate (devices and capacity) from the storage devices brought under management of the Storage Spaces Direct configuration. The remainder of the storage devices is placed in a single pool of storage capacity regardless of the number of servers in the Scale Unit.<br>

## **Recommended documents**

[Azure Stack storage capacity planning](https://docs.microsoft.com/azure/azure-stack/capacity-planning-storage)