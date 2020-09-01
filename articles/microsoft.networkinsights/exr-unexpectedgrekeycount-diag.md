<properties
pageTitle="Unexpected GRE Key Count"
description="Unexpected GRE Key Count."
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors=""
displayOrder="10"
articleId="ExRRnmBrooklynConsistencyUnexpectedGreKeyCountInsight"
diagnosticScenario="ExRRnmBrooklynConsistencyUnexpectedGreKeyCountInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute Configuration Issue Detected
<!--issueDescription-->
We have identified an Azure platform configuration issue for your private peering ExpressRoute connection to virtual network ID: **<!--$VNetId-->[VNetId]<!--/$VNetId-->**. The initial diagnosis is showing that your Virtual Network Gateway for this virtual network is receiving an unexpected General Routing Encapsulation (GRE) key count. See below for more details and steps for mitigation.
<!--/issueDescription-->
## **Mitigation Steps**
We are working with the appropriate teams to mitigate this issue as quickly as possible and return you to normal operations. If you would prefer to forfeit a detailed root cause analysis and expedite the resolution of connectivity consider removing and re-creating the ExpressRoute Connection in the [Azure portal](http://portal.azure.com) and [resetting the gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic). 

Microsoft is continuously working to identify and resolve issues proactively.  We will contact you as soon as the issue is mitigated to ensure you're no longer impacted.  Please feel free to reach out with any questions in the meantime.  Again, we apologize for the inconvenience. 
