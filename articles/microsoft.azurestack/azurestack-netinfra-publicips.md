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

# Azure Stack Add Public IPs

You can add Public IP addresses to your Azure Stack system at any time after the initial deployment of the Azure Stack system. 

If you are trying to remove public IPs instead, contact support by opening a case.

## **Recommended Steps**

To add public IPs to your Azure Stack environment, follow these steps:

1. [Obtain the address block from your provider](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-ips#obtain-the-address-block-from-your-provider)
2. [Add the IP address range to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-ips#add-the-ip-address-range-to-azure-stack)
3. [Update the ACLs on your top-of-rack switches](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-ips#update-the-acls-on-your-top-of-rack-switches)

## **Recommended Documents**

* [Networking Considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
* [View Public IP Address Consumption in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-viewing-public-ip-address-consumption)
* [REST API to list Public IP Addresses](https://docs.microsoft.com/rest/api/azurestack/publicipaddresses/list)
* [Add Public IP Addresses to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-ips)