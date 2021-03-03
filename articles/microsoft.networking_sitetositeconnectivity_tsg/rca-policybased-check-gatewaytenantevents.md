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
	articleId="5f1c7e82-b601-4b31-b73c-b3c681212e27"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Check the Gateway Tenant Events

## **Recommended Steps**

* Check the Gateway Tenant Events. This logs can be pulled for an entire day as it logs any events triggered by tenant

*for e.g., https://jarvis-west.dc.ad.msft.net/34C512B7*

*<?xml version="1.0"?> <NameValues Detail="Operation NodeStateChanged: Configured GW successfully" />*

*<?xml version="1.0"?> <NameValues Detail="GatewayTenant service role started" />*

*<?xml version="1.0"?><NameValues Detail="Site 80320078-1322-41f0-9f6d-21b17b00d548 connectivity state changed from Connecting to Connected state." />*

## **Recommended Documents**