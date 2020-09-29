<properties
	pageTitle="Check if customer is exceeding the maximum number of Security Associations"
	description="Check if customer is exceeding the maximum number of Security Associations"
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
	articleId="87dfe0de-862f-46ad-833b-661ed44faaae"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# How to check if customer is exceeding the maximum number of Security Associations

## **Recommended Steps**

* Azure VPN gateway limit of 200 subnet SA pairs.
* Calculate the # of Azure Vnet subnets multiplied times the # of local subnets defined in 'local network gateway' object is greater than 200 the customer will see sporadic subnets disconnecting
