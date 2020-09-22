<properties
    pageTitle="Deploy Azure Firewall with multiple public IP addresses"
    description="Deploy Azure Firewall with multiple public IP addresses"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745459"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="131add25-127d-40b4-b5a5-5d50927360ef"
/>

# Deploy Azure Firewall with multiple public IP addresses

Deploying multiple IP enables the following scenarios:

## DNAT

You can translate multiple standard port instances to your backend servers. For example, if you have two public IP addresses, you can translate TCP port 3389 (RDP) for both IP addresses.

## SNAT

Additional ports are available for outbound SNAT connections, reducing the potential for SNAT port exhaustion. Currently, Azure Firewall randomly selects the source public IP address to use for a connection. If you have any downstream filtering on your network, you need to allow all public IP addresses associated with your firewall. Consider using a public IP address prefix to simplify this configuration. Use the following PowerShell samples to configure Azure Firewall with multiple public IPs.

## **Recommended Documents**

- [Create an Azure firewall](https://docs.microsoft.com/azure/firewall/deploy-multi-public-ip-powershell#create-a-firewall-with-two-or-more-public-ip-addresses) with two or more public IP addresses
- [Add a public IP address](https://docs.microsoft.com/azure/firewall/deploy-multi-public-ip-powershell#add-a-public-ip-address-to-an-existing-firewall) to an existing Azure firewall
- [Remove a public IP address](https://docs.microsoft.com/azure/firewall/deploy-multi-public-ip-powershell#remove-a-public-ip-address-from-an-existing-firewall) from an existing Azure firewall
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues)
