<properties
	pageTitle="Lifetime change QM Notify"
	description="Lifetime change QM Notify"
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
	articleId="322f351f-83ee-4f54-b06a-a6c4197abc62"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Lifetime change QM Notify

## **Recommended Steps**

* The on-prem device is trying to change a connection parameter after the Main Mode is already established.
* This is not supported by our gateway.
* The customer needs to fix their on-prem device to establish the IPsec session directly with the final settings we want to use.
* Often times, this is caused by the on-prem device missing the Lifetime in bytes setting.
  