<properties
	pageTitle="DOS Mode On"
	description="DOS Mode On"
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
	articleId="bd4fa36d-b15b-4dd4-861b-e41e6647be89"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# DOS Mode On

## **Recommended Steps**

* The IPsec stack on the Windows OS is in DoS mode - it will stop accepting connection attempts
* This happens when there are more than 500 outstanding (incomplete) security associations
* This usually happens when the on-prem device has an issue and starts creating a security association, Azure starts replying, but the on-prem device stops responding
* Resetting the Azure VPN gateway will NOT help because after the reset, the on-prem device will still create Incomplete SAs
* The mitigation will involve a reboot of the on-prem device
