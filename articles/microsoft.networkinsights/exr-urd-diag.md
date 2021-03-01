<properties
pageTitle="Gateway Subnet UDR 2"
description="ExpressRoute gateway subnet has UDR applied"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="genlin"
ms.author="mariliu"
articleId="ExRVnetGatewayUdrOnGatewaySubnetInsightForNullNextHop"
selfHelpType="Diagnostics"
resourceTags="windows"
supportTopicIds="32602123, 32627985"
productPesIds="15480"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute gateway subnet has UDR applied
<!--issueDescription-->
We have detected user-defined routes (UDRs) **<!--$UDRStrings-->UDRStrings<!--/$UDRStrings-->** in the gateway subnet of your ExpressRoute virtual network gateway **<!--$GatewayName-->GatewayName<!--/$GatewayName-->**. Traffic that’s routed to a Next Hop Type of `None` or `Null` by using UDR will cause dropped traffic.
<!--/issueDescription-->

## **Recommended Steps**

Review the UDRs in the gateway subnets that have a Next Hop Type of `None` or `Null`. Remove any that are causing unintended traffic drops.
