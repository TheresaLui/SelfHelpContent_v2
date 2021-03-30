<properties
    pageTitle="ExpressRoute Direct is down"
    description="ExpressRoute Direct is down"
    infoBubbleText="Need more information about this issue? See details on the right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    articleId="ExpressRouteDirectDown"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    supportTopicIds="32627976"
    resourceTags=""
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute Direct is down
<!--issueDescription-->
We have identified that the line protocol or the physical connectivity for one or both links of your ExpressRoute Direct resources **[Azure resource name]** is down. Line protocol/physical connectivity is up when (1) admin state is enabled on both ports and (2) transmit and receive light levels are within an acceptable range.
<!--/issueDescription-->

## **Recommended Steps**

- Make sure admin state is enabled on both links of your ExpressRoute Direct resource **[Azure resource name]** as well as your on-premises port pair. Refer to [How to Configure ExpressRoute Direct](https://docs.microsoft.com/azure/expressroute/how-to-expressroute-direct-portal) for assistance.
- Review the transmit and receive light levels on the Microsoft Enterprise Edge (MSEE) device pair and on-premises. For assistance viewing transmit and receive light on ExpressRoute Direct, refer to [ExpressRoute monitoring, metrics and alerts](https://docs.microsoft.com/azure/expressroute/expressroute-monitoring-metrics-alerts#expressroute-direct-metrics). If the MSEE and on-premises ports are transmitting but not receiving light levels, you may need to request the co-location provider to roll the fiber cross connections.
