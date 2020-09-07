<properties
    pageTitle="Customer configured Private Address Ranges for No Source NAT"
    description="Customer configured Private Address Ranges for No Source NAT"
    service="microsoft.network"
    resource=""
    authors="gopimsft"
    ms.author="gopimsft"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32731149"
    resourceTags=""
    productPesIds="16556"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="customer-configured-private-address-ranges-for-no-source-nat"
	ownershipId="CloudNet_AzureFirewall"
/>
# Customer configured Private Address Ranges for No Source NAT

## **Recommended Steps**

Azure firewall provides automatic Source Network Address Translation (SNAT) for all outbound traffic to public IP addresses. Azure Firewall doesn’t SNAT when the destination IP address is a private IP address range per IANA RFC 1918. If your organization uses a public IP address range for private networks or opts to force tunnel Azure Firewall internet traffic via an on-premises firewall, you can configure Azure Firewall to not SNAT additional custom IP address ranges. For more information, see [Azure Firewall SNAT private IP address ranges](https://docs.microsoft.com/azure/firewall/snat-private-range).
