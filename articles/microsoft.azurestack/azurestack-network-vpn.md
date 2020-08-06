<properties
    pageTitle="Azure Stack Hub VPN for User Environment"
    description="Azure Stack Hub VPN for User Environment"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629282"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-network-vpn"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub VPN for User Environment

## **Recommended Steps**

Create a site-to-site VPN to connect a virtual network in Azure Stack Hub to a virtual network in Azure or to an on-premises workload:

1. First, review [VPN service differences on Azure Stack Hub](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
1. [Troubleshoot site-to-site VPN connections](https://docs.microsoft.com/azure-stack/user/azure-stack-vpn-gateway-settings)
1. [Troubleshoot Network Virtual appliance (NVA) VPN connections](https://docs.microsoft.com/azure-stack/user/network-virtual-appliance)
1. [Test the connection](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#test-the-connection)

For sample configurations on 3rd party devices, see [VPN devices and IPsec/IKE parameters for Site-to-Site VPN Gateway connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices).

With the right network connectivity, a site-to-site VPN connection can also be used to connect a virtual network in Azure Stack Hub to ExpressRoute. For more details about hybrid connectivity, see [Hybrid connectivity options](https://docs.microsoft.com/azure-stack/operator/azure-stack-datacenter-integration?view=azs-1908#hybrid-connectivity-options).

## **Recommended Documents**

* [Connect Azure Stack Hub to Azure using VPN](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn)
* [IPSec/IKE parameters for Azure Stack Hub](https://docs.microsoft.com/azure-stack/user/azure-stack-vpn-gateway-settings#ipsecike-parameters)
* [VPN gateway configuration settings for Azure Stack Hub](https://docs.microsoft.com/azure/azure-stack/azure-stack-vpn-gateway-settings)
* [About VPN devices and IPsec/IKE parameters for Site-to-Site VPN Gateway connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices)
