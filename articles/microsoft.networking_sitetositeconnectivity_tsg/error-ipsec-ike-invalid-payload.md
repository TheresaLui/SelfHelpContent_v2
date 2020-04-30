<properties
	pageTitle="IKE Payload is Invalid"
	description="IKE Payload is Invalid"
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
	articleId="4c64e0b4-fe08-45af-a99b-11ea0d087abe"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Payload is Invalid

## **Recommended Steps**

* IKE payload is invalid
* The on-prem device is sending an incorrect IKE payload
* Tell customer to engage the third-party device vendor
* When Azure is initiator, and if the peer only accepts narrow traffic selectors, the following message will be logged in IkeLogsTable/TunnelInsightsEventTable **Invalid payload received**

	* To fix this, please configure narrow Traffic Selectors on Azure VPN Gateway
