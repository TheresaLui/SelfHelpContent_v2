<properties
    pageTitle="Integrate Azure Firewall with Azure Standard Load Balancer"
    description="Integrate Azure Firewall with Azure Standard Load Balancer"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745452, 32745461"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="218d411a-91fa-4aa7-89e7-80c15752ae61"
/>

# Integrate Azure Firewall with Azure Standard Load Balancer

The preferred design is to integrate an internal load balancer with your Azure firewall, as this is a much simpler design.

You can use a public load balancer if you already have one deployed and you want to keep it in place. However, you need to be aware of an asymmetric routing issue that can break functionality with the public load balancer scenario.

## **Recommended Documents**

Use the below links to configure appropriately.

- Integrate with [public load balancer](https://docs.microsoft.com/azure/firewall/integrate-lb#public-load-balancer).
- Integrate with [Internal load balancer](https://docs.microsoft.com/azure/firewall/integrate-lb#internal-load-balancer).
- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
