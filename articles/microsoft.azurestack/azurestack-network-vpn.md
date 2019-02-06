<properties
    pageTitle="Azure Stack VPN"
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
    cloudEnvironments="public"
    articleId="azurestack-network-vpn"
/>

# Azure Stack VPN

Create a site-to-site VPN to connect a virtual network in Azure Stack to a virtual network in Azure.

## **Recommended steps**

1. [Create the network resources in Azure](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-the-network-resources-in-azure)
2. [Create the connection](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-the-connection)
3. [Create a virtual machine](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-a-virtual-machine)
4. [Create the network resources in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#create-the-network-resources-in-azure-stack)
5. [Test the connection](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn#test-the-connection)

For 3rd party device sample configurations see documentation for [VPN devices and IPsec/IKE parameters for Site-to-Site VPN Gateway connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices).

Ensure that you enable [site-to-site (S2S) protocols ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#can-i-traverse-proxies-and-firewalls-using-point-to-site-capability) on firewall devices in your public Virtual IP network.

## **Recommended documents**

* [Connect Azure Stack to Azure using VPN](https://docs.microsoft.com/azure/azure-stack/azure-stack-connect-vpn)
* [About VPN gateway for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-vpn-gateway-about-vpn-gateways)
* [VPN gateway configuration settings for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-vpn-gateway-settings)
* [About VPN devices and IPsec/IKE parameters for Site-to-Site VPN Gateway connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices)