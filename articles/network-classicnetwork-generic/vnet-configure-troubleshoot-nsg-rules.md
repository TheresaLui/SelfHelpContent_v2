<properties
    pageTitle="Azure Virtual Network - Configure and troubleshoot NSG rules"
    description="Azure Virtual Network - Configure and troubleshoot NSG rules"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781385"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="086ee5d6-5758-4aff-bbea-330a99ca5c76"
/>

# Azure Virtual Network - Configure and troubleshoot NSG rules

## **Recommended Steps**

1. Block access to the Internet for your subnet or virtual machine (VM), using the following rule properties and Internet Service Tag:

   Source: 0.0.0.0/0
   Source Ports: 0-65535
   Destination: Internet
   Destination Ports: 0-65535
   Protocol: Any
   Access: Deny

   To allow traffic for specific services and destinations to bypass this, specify an Allow rule with higher priority for your desired internet protocols (IPs) or Service Tags.

2. You can't currently create rules to filter traffic from specific Fully Qualified Domain Names (FQDNs). To find updated status on this feature ask, check [this feedback item]( https://feedback.azure.com/forums/217313-networking/suggestions/17357071-allow-creation-of-nsg-rules-based-on-fqdn-along-wi). Configure FQDN application rules to filter traffic in an [Azure Firewall]( https://docs.microsoft.com/azure/firewall/features#application-fqdn-filtering-rules).

3. [Learn how](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview#security-rules) to create rules with specific source and destination IPs and ports

4. Check that you are not trying to create a rule with the same priority and direction as an already existing rule in your network security group (NSG)

5. Check the [updated list of Service Tag IP ranges](https://docs.microsoft.com/azure/virtual-network/service-tags-overview#discover-service-tags-by-using-downloadable-json-files) to make sure you understand which IPs you are allowing by using rules with certain Service Tags

6. [Learn how]( https://docs.microsoft.com/azure/virtual-network/diagnose-network-traffic-filter-problem) to diagnose why traffic is being incorrectly blocked or allowed

7. [Learn how]( https://docs.microsoft.com/azure/virtual-network/network-security-group-how-it-works#intra-subnet-traffic) to understand how NSG rules work within subnets

## **Recommended Documents**

- [Filtering NSG traffic correctly](https://docs.microsoft.com/azure/virtual-network/network-security-group-how-it-works)
- [Understanding NSGs](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview)
- [Understanding ASGs](https://docs.microsoft.com/azure/virtual-network/application-security-groups)
