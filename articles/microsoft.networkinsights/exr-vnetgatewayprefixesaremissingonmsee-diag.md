<properties
pageTitle="Express Route VNet Gateway Prefixes Are Missing On MSEE"
description="Express Route VNet Gateway Prefixes Are Missing On MSEE"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors=""
displayOrder="10"
articleId="ExRVNetGatewayPrefixesMissingOnMseeInsight"
diagnosticScenario="ExRVNetGatewayPrefixesMissingOnMseeInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute Configuration Issue Detected
<!--issueDescription-->
We have identified an Azure platform configuration issue for your private peering ExpressRoute connection with a service key of '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'. The initial diagnosis is showing that the Microsoft Edger Router is missing prefixes from your Virtual Network Gateway. See below for more details and steps to mitigate.
<!--/issueDescription-->
**Mitigation Steps**
We are working with the appropriate teams to mitigate this issue as quickly as possible and return you to normal operations. If you would prefer to forfeit a detailed root cause analysis and expedite the resolution of connectivity consider removing and re-creating the ExpressRoute Connection in the [Azure portal](http://portal.azure.com) and [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). 

Microsoft is continuously working to identify and resolve issues proactively.  We will contact you as soon as the issue is mitigated to ensure you're no longer impacted.  Please feel free to reach out with any questions in the meantime.  Again, we apologize for the inconvenience. 
