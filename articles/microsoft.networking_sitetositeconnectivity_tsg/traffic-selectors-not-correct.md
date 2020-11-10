<properties
	pageTitle="Use of traffic selectors"
	description="Use of traffic selectors"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="04b7f460-a968-475a-a930-78674566267f"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Use of traffic selectors

## **Recommended Steps**

* If narrow traffic selectors aren't being used, it means that the Azure VPN Gateway is configured to use 0.0.0.0/0 <-> 0.0.0.0/0 traffic selectors.
* However, the on-prem device may still narrow down the Traffic Selectors
* Review IkeLogs/ SeamlessTunnelServiceTraceTable in ASC or Jarvis/Kusto from the time of the issue to see which side is using traffic selectors.
