<properties
    pageTitle="Filter traffic based on IP address using network rule collections"
    description="Filter traffic based on IP address using network rule collections"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745460"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="142b0b09-6d59-470c-b1c3-de4f54273b7f"
/>

# Filter traffic based on IP address using network rule collections

You can centrally create allow or deny network filtering rules by source and destination IP address, port, and protocol.

Azure Firewall is fully stateful, so it can distinguish legitimate packets for different types of connections. Rules are enforced and logged across multiple subscriptions and virtual networks.

## **Recommended Documents**

- Use the Azure Portal to [configure network rules](https://docs.microsoft.com/azure/firewall/tutorial-hybrid-portal#configure-network-rules).
- Use [Service tag in network](https://docs.microsoft.com/azure/firewall/service-tags) rules to help minimize complexity for security rule creation.
- Use [IP Groups](https://docs.microsoft.com/azure/firewall/ip-groups) to group and manage IP addresses for Azure Firewall rules.
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
