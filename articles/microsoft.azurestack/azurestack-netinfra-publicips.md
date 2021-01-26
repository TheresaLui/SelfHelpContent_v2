<properties
    pageTitle="Azure Stack Add or Remove Public IPs"
    description="Add or Remove Public IP to Pool"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629189"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-network-publicips"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Add or remove a public IP to a pool in Azure Stack

You can add public IP addresses to your Azure Stack system at any time after the initial deployment.

If you are trying to remove public IPs instead, contact support by opening a case.

## **Recommended Steps**

To add public IPs to your Azure Stack environment, follow these steps:
1. Obtain the address block from your provider
2. Add the IP address range to Azure Stack
3. Update the ACLs on your top-of-rack switches

For more detailed instructions, see [Add the IP address range to Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-ips#add-the-ip-address-range-to-azure-stack-hub).

## **Recommended Documents**

* [Networking considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* [View Public IP Address Consumption in Azure Stack](https://docs.microsoft.com/azure-stack/operator/azure-stack-viewing-public-ip-address-consumption#view-public-ip-address-consumption-in-azure-stack-hub)
* [REST API to list public IP addresses](https://docs.microsoft.com/rest/api/azurestack/publicipaddresses/list)
* [Logical networks or public IPs](https://docs.microsoft.com/azure-stack/operator/azure-stack-network?view=azs-2002#logical-networks)
