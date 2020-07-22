<properties
    pageTitle="Latency issues with Traffic via Azure Firewall"
    description="Latency issues with Traffic via Azure Firewall"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745464"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="a0ccb8a7-944f-4957-9af0-fa5cf1a98402"
/>

# Latency issues with Traffic via Azure Firewall

Follow the deployment guidance to get the best performance and latency when using Azure Firewall.

You can deploy Azure Firewall on any virtual network, but customers typically deploy it on a central virtual network and peer other virtual networks to it in a hub-and-spoke model. Set the default route from the peered virtual networks to point to this central firewall virtual network. Global VNET peering is supported, but it is not recommended because of potential performance and latency issues across regions. For best performance, deploy one firewall per region.

The advantage of this model is the ability to centrally exert control on multiple spoke VNETs across different subscriptions. There are also cost savings as you do not need to deploy a firewall in each VNET separately. The cost savings should be measured versus the associate peering cost based on the customer traffic patterns.

## **Recommended Documents**

- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
