<properties
pageTitle="ExpressRoute Gateway Has undergone host OS maintenance"
description="Provides the solution to the problem in which ExpressRoute Gateway Has undergone host OS maintenance."
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="genlin"
ms.author="mariliu"
articleId="hostosmaintenance"
selfHelpType="Diagnostics"
resourceTags="windows"
supportTopicIds="32602123, 32627985"
productPesIds="15480"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute Gateway Has undergone host OS maintenance
<!--issueDescription-->
We have identified that your ExpressRoute gateway resource **[Gateway Name]** has undergone OS maintenance within the last 30 days. The ExpressRoute gateway includes multiple instances, and one or more instances of your gateway resource is taken offline during maintenance. Although this may cause your gateway to temporarily support lower network throughput to the virtual network, the gateway itself will not experience any downtime.
**[Gateway Update Data Table]**
<!--/issueDescription-->

## **Recommended Steps**
- If you experienced intermittent connectivity issues within the last 30 days, your gateway may be overused. Therefore, it cannot function correctly with one less instance. Consider [upgrading your gateway SKU](https://docs.microsoft.com/azure/expressroute/expressroute-about-virtual-network-gateways#gwsku) to support higher network throughput and maintain consistency in performance during OS maintenance. 
- If you experienced an outage within the last 30 days, please submit a support request in the Azure portal for more help.
