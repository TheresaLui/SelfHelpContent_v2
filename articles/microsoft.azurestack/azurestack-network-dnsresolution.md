<properties
    pageTitle="Azure Stack DNS resolution for User environment"
    description="Resolve issues with Azure Stack DNS resolution"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629210"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="azurestack-network-dnsresolution"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Resolve issues with Azure Stack VM DNS resolution

By default, tenant VMs deployed in Azure Stack will have name resolution for other VMs within the same Virtual Network (VNet), as well as external addresses on the internet.

When resources deployed in virtual networks need to resolve domain names to internal IP addresses, they can use one of two methods:

**Azure-provided name resolution** for public Internet addresses, and for VMs and role instances that reside within the same virtual network or cloud service.

**Name resolution that uses your own DNS server** to support additional scenarios, such as:

* Create a DNS record under an existing hosted DNS zone, for example, local.azurestack.external
* Create a DNS zone, such as contoso.com
* Create a record under your own custom DNS zone
* Support the purchase of domain names

## **Recommended Steps**

* Become familiar with the differences in Azure Stack in [comparison with Azure DNS](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-dns#comparison-with-azure-dns)
* Use [DNS hostname resolution](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-dns#support-for-dns-hostname-resolution) and [create and manage DNS zones and records using the API](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-dns#create-and-manage-dns-zones-and-records-using-the-api)
* Use [iDNS for Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-understanding-dns) to resolve internet DNS names and other VMs in the same virtual network

## **Recommended Documents**

* [Name resolution for resources in Azure virtual networks](https://docs.microsoft.com/azure/virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances)
* [Using DNS in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-dns)
* [Introducing iDNS for Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-understanding-dns)
* [Azure Stack Networking Considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
