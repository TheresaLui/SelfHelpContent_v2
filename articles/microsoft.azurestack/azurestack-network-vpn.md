<properties
    pageTitle="Azure Stack VPN for User Environment"
    description="Azure Stack VPN for User Environment"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629282"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="azurestack-network-vpn"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack VPN for User Environment

## **Recommended Steps**

Create a site-to-site VPN to connect a virtual network in Azure Stack to a virtual network in Azure:

1. First, review [VPN service differences on Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-network-differences)
2. [Create the network resources in Azure](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-the-network-resources-in-azure)
3. [Create the connection](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-the-connection)
4. [Create VPN gateways for Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-vpn-gateway-about-vpn-gateways)
5. [Create the network resources in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-the-network-resources-in-azure-stack)
6. [Test the connection](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#test-the-connection)

Ensure that you enable [site-to-site (S2S) protocols ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#can-i-traverse-proxies-and-firewalls-using-point-to-site-capability) on firewall devices in your public Virtual IP network used by Azure Stack. For sample configurations on 3rd party devices, see [VPN devices and IPsec/IKE parameters for Site-to-Site VPN Gateway connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices).

 With the right network connectivity, a site-to-site VPN connection can also be used to connect a virtual network in Azure Stack to a ExpressRoute. For more details about hybrid connectivity, see [Hybrid connectivity options](https://docs.microsoft.com/azure-stack/operator/azure-stack-datacenter-integration?view=azs-1908#hybrid-connectivity-options).

## **Recommended Documents**

* [Connect Azure Stack to Azure using VPN](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn)
* [VPN gateway settings for Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-vpn-gateway-settings#vpn-gateway-settings)
* [IPSec/IKE parameters for Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-vpn-gateway-settings#ipsecike-parameters)
* [VPN gateway configuration settings for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-vpn-gateway-settings)
* [About VPN devices and IPsec/IKE parameters for Site-to-Site VPN Gateway connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices)
