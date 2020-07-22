<properties
    pageTitle="Traffic via Azure Firewall is blocked"
    description="Traffic via Azure Firewall is blocked"
    service="microsoft.network"
    resource="azurefirewalls"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32745454, 32745474"
    resourceTags=""
    productPesIds="16556"
    ownershipId="CloudNet_AzureFirewall"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="ff772dd2-754d-4080-b1a5-037157440cf4"
/>

# Traffic via Azure Firewall is blocked

## **Recommended Steps**

Connectivity via Azure Firewall could be blocked because of either asymmetric routing or non-existent **Allow** rules. To fix this issue, perform the following steps:

1. Verify that Subnet is configured to forward traffic to Azure Firewall. Also verify that the Virtual machines running in Azure has the default route `(0.0.0.0/0)` configured to Azure Firewall with the [effective routes](https://docs.microsoft.com/azure/virtual-network/manage-route-table#view-effective-routes). Use Azure Portal to [add default routes](https://docs.microsoft.com/azure/firewall/tutorial-firewall-deploy-portal#create-a-default-route) to subnets.
1. Ensure that there is no asymmetric routing between source and destination. Asymmetric routing occurs when a packet takes one path to the destination and takes another path when returning to the source. Virtual networks must be configured with default route to Azure Firewall.
1. Follow the instructions provided in [the step-by-step guide](https://docs.microsoft.com/azure/firewall/tutorial-hybrid-portal#prerequisites) to asymmetric routing, to connect deployments which use Virtual network gateway on-premise.
1. Verify that deployments which use public [load balancer](https://docs.microsoft.com/azure/firewall/integrate-lb#public-load-balancer), follow load balancer configuration.
1. Use Azure Portal to [configure a firewall rule](https://docs.microsoft.com/azure/firewall/tutorial-hybrid-portal#configure-network-rules) to route traffic between source and destination.
1. Use Firewall logs to [monitor Azure Firewall](https://docs.microsoft.com/azure/firewall/logs-and-metrics) and confirm that traffic is flowing through Azure Firewall.

## **Recommended Documents**

- Learn more about [Azure Firewall](https://docs.microsoft.com/azure/firewall/overview), [Firewall FAQs](https://docs.microsoft.com/azure/firewall/firewall-faq) and [known issues](https://docs.microsoft.com/azure/firewall/overview#known-issues).
