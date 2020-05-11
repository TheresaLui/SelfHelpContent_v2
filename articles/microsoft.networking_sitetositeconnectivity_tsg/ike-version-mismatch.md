<properties
	pageTitle="IKE Version Mismatch"
	description="IKE Version Mismatch"
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
	articleId="1f40a10f-d193-435e-b99e-6f34e54e14a1"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Version Mismatch

## **Recommended Steps**

* If the customer is running Policy Based Gateways, verify that the on-prem device is configured to use IKEv1.
* If instead this is a Route Based Gateways, verify that the onprem device is configured to use IKEv2.
