<properties
	pageTitle="Can not determine error"
	description="Can not determine error"
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
	articleId="2cdc0734-97bd-417d-acbe-dbb6cbd9c07a"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Cannot determine error

## **Recommended Steps**

* As the gateway is healthy and successfully responds to DIP probes, but it wasn’t possible to collect diagnostics, we can not determine what is the error causing the IPsec issue because of lack of data
* This can happen in the following situations:

	* The customer’s issue happened in the past but we don’t have a trace at the time. In this case, no RCA is possible. We need to have a trace during the issue for Policy Based gateways.
	* There are known issues with log collection. Please double check with your Technical Advisor if you did not find logs.
