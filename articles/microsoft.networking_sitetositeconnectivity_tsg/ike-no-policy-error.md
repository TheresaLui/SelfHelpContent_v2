﻿<properties
	pageTitle="Gateway not sending IPsec traffic"
	description="Gateway not sending IPsec traffic"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="199f28b5-e8b6-4404-be2f-b74e34411832"
/>

# Gateway not sending IPsec traffic

The Azure VPN gateway is not initiating IKE traffic and/or is not responding at all to the on-prem device connection attempts. In this scenario, the issue is that the gateway tenant is not configured to connect to this specific on-prem device (in some circumstances, this could cause the gateway to load the "default" policy that uses Certificate authentication rather than PSK – this is a good pointer in the logs). Reasons for this may include:

* The IP address of the on-prem device may be incorrect. Fix the IP address.
* The customer might have not created a connection object. Create one.
* The SiteConnectivityAction flag is set to Disconnect. Change it to Connect using the link below.
* The customer might have configured everything correctly, but the gateway tenant may still miss to be properly configured.

## Private Links

1. https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki?pageId=134283&&anchor=siteconnectivityaction-flag-set-to-disconnect
