<properties 
    pageTitle="I can't resolve a DNS record from private DNS zone"
    description="I am unable to resolve a new DNS record in a DNS zone hosted in Azure DNS."
    service="microsoft.network"
    resource="privateDnsZones"
    authors="rohinkoul"
    ms.author="rohink"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	articleId="privatedns-cantresolverecord"
	ownershipId="CloudNet_DNS"
/>

# I can't resolve DNS records from a private DNS zone

## **Recommended Steps**

DNS name resolution is a multi-step process, which can fail for many reasons. The following steps help you investigate why DNS resolution is failing for a DNS record in a zone hosted in Azure DNS.

* Confirm that the DNS records have been configured correctly in Azure DNS private zones. Review the DNS records in the Azure portal, checking that the zone name, record name, and record type are correct.
* Confirm that the virtual network is linked to the private DNS zone. Check the **"Virtual network links"** tab under private DNS zone and make sure that the link to virtual network is listed there.
* If the domain name you are trying to resolve ends in **".local"**, please check if you are able to resolve from a private DNS zone that does not end in ".local"? Domain names ending in ".local" are reserved for multicast DNS. Although creation of such domain is supported by Azure DNS private zones, some operating systems may not resolve these names as expected. Please create a new DNS zone that does not end in ".local" or check the documentation of the operating system used by your virtual machines on how to disable multicast DNS in virtual machine.
* Ensure that you are using Fully Qualified Domain Name (FQDN) while querying the Azure DNS private zones. If you are using single label names please make sure that you have configured **correct DNS suffix** on your [Windows](https://docs.microsoft.com/azure/virtual-network/virtual-networks-name-resolution-ddns#windows-clients) or [Linux](https://docs.microsoft.com/azure/virtual-network/virtual-networks-name-resolution-ddns#linux-clients) virtual machines.
* If you are using **custom DNS Servers** with in your virtual network, please make sure that these servers are forwarding DNS queries to Azure resolver (168.129.63.16) for private DNS zones hosted in Azure DNS
* DNS resolution against Azure DNS private zones from **PaaS applications** injected in a virtual network is not supported natively. To workaround this problem:

  * Deploy a custom DNS server (VM based) in the virtual network where you have injected the application
  * Configure the DNS server to forward traffic to 168.129.63.16 (Azure resolver)
  * Go to the DNS server settings on the virtual network and enter the IP address of the DNS servers deployed by you
  * Execute a [Sync Network](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#managing-vnet-integration) operation on the injected PaaS application for the changes to take effect
