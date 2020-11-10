<properties
	pageTitle="Check for the Use of traffic selectors"
	description="Check for the Use of traffic selectors"
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
	articleId="7c48e111-ce99-4ebd-a199-d8be7c87b946"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# How to check for the Use of traffic selectors

## **Recommended Steps**

* In this scenario, there are Traffic Selectors in place that are only allowing connectivity to certain subnets and not to others
* Notice that usage of such limited traffic selectors may not prevent the VPN tunnel from correctly establishing, but will only block traffic from flowing
* The traffic selectors may exist on the Azure configuration or the customer configuration
* Traffic Selector configuration should match both sides in the Azure Site-to-Site VPN. By default, in a route-based VPN, Azure is configured to accept 0.0.0.0/0; however, if the peer site is configured with a narrow Traffic Selector, the connection will not establish while Azure is the initiator. Make sure that the Traffic Selectors match both sides.
* If you need to view Traffic Selectors, review IkeLogs table from ASC/Jarvis/Kusto 

## **Recommended Documents**  

* [Jarvis](https://jarvis-west.dc.ad.msft.net/47F4EC8E)
* Kusto: cluster('Aznw').database('aznwmds').IkeLogsTable
