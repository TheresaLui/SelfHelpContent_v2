<properties
pageTitle="ExpressRoute Gateway CPU Utilization is high"
description="Provides the solution to the problem in which ExpressRoute Gateway CPU Utilization is high"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="genlin"
ms.author="mariliu"
articleId="highcpu"
selfHelpType="Diagnostics"
resourceTags="windows"
supportTopicIds="32539947"
productPesIds="15480"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute Gateway CPU Utilization is high
<!--issueDescription-->
We have identified that your ExpressRoute gateway resource **[Gateway Name]** has recently experienced high CPU use. Your current gateway SKU might not be able to support the current workload. This may cause performance issues when you send traffic from your on-premises resources to virtual machines (VMs) on private endpoints in the Azure Virtual Network.
<!--/issueDescription-->

## **Recommended Steps**
- Review the number of routes that you are advertising from on-premises, and the frequency at which you change these routes. Advertising many routes or frequently changing the advertised routes might increase your gateway CPU use. Therefore, consider reducing the number of routes or the frequency at which you change the advertised routes.
- If you are experiencing performance issues, consider [upgrading your gateway SKU](https://docs.microsoft.com/azure/expressroute/expressroute-about-virtual-network-gateways#gwsku) to support higher network throughput.
- If your gateway continues to report high CPU use, and you still experience performance issues, please submit a support request in the Azure portal for more help.

