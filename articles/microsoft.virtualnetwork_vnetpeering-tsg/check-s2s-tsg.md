<properties
	pageTitle="TSG Content Step: Check S2S TSG"
	description="TSG Content Step: Check S2S TSG"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public"
	articleId="72ba7550-9273-4d91-8b1c-160ef5d75ac0"
/>

# Referral to site-to-site troubleshooting guide

The customer is not able to connect from their on-premises resources to resources within the VNet that has the VPN gateway (or ExR). This indicates that there is a problem with the basic VPN connection that must be addressed first before troubleshooting the the VNet peering gateway transit aspect.

## **Recommended Steps**

1. Resolve the customer's site-to-site connectivity issue to the resources in the VNet that has the VPN site-to-site gateway using the [Site-to-site TSG](https://aka.ms/VpnS2sConnectivityTSG)
2. Come back to this [Vnet Peering TSG](https://aka.ms/VNetPeeringTSG) when the site-to-site issue is resolved

