<properties
	pageTitle="Check Brooklyn Diagnostic Logs for Route Based VPN"
	description="Check Brooklyn Diagnostic Logs for Route Based VPN"
	service="microsoft.network"
	resource="vpnGateways"
	authors="riturajc"
	ms.author="arshads, riturajc, sushrao"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="83cc9674-b855-4064-bc7e-e7b580e54d6f"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Check the Asyncworkerlogs

## **Recommended Steps**

*This can help us to determine what could have caused the events to get triggered by using the above timeline*

*https://jarvis-west.dc.ad.msft.net/C9C0D1FB*

*Search for ExecuteOperation:*

*Code: Microsoft.CloudNet.GatewayManager.AsyncWorkItems.PutGatewayConnectionWorkItem*

*Microsoft.CloudNet.GatewayManager.AsyncWorkItems.PutGatewayWorkItem*

*Code: Microsoft.CloudNet.GatewayManager.AsyncWorkItems.UpgradeGateway*

*Code: Microsoft.CloudNet.GatewayManager.AsyncWorkItems.ResetGateway*

*Code: Microsoft.CloudNet.GatewayManager.AsyncWorkItems.SetConfigurationWorkItem*

## **Recommended Documents**