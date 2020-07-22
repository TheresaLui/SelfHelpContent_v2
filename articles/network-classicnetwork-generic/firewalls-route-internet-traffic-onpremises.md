<properties
    pageTitle="Configure Azure Firewall to route Internet traffic to on-premises firewall"
    description="Configure Azure Firewall to route Internet traffic to on-premises firewall"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745457"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="4f6c5d0b-5c2d-45e0-ba5f-756ecaa76522"
/>

# Configure Azure Firewall to route Internet traffic to on-premises firewall

When you configure a new Azure Firewall, you can route all Internet-bound traffic to a designated next hop instead of going directly to the Internet. For example, you may have an on-premises edge firewall or other network virtual appliance (NVA) to process network traffic before it is passed to the Internet. However, you cannot configure an existing firewall for forced tunneling.

Note that private traffic ranges are configured alongside Forced Tunneling configuration to avoid Internet-bound traffic from being SNATed to one of the firewall private IP addresses in AzureFirewallSubnet, hiding the source from your on-premises firewall.

## **Recommended Documents**

- Configure [Forced Tunneling](https://docs.microsoft.com/azure/firewall/forced-tunneling).
- Learn more about [SNAT private IP address ranges](https://docs.microsoft.com/azure/firewall/snat-private-range).
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
