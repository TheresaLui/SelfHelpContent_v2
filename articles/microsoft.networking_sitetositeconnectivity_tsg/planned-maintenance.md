<properties
	pageTitle="Planned Maintenance"
	description="Planned Maintenance"
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
	articleId="542836b5-d407-4c33-87fc-2957a83f4f26"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Planned Maintenance

## **Recommended Steps**

* Please remember that our gateways would trigger a failover proactively for every Host maintenance event and this is a new change to reduce the over all downtime.  Traditionally we were depending on SLB time-out to trigger the failover which introduced more delays.
* Inform the customer the Disconnection is caused by planned maintenance.
* If the tunnel has not returned to an operational state, then please restart the TSG and select the "VPN doesnt connect" troubleshooting path
  