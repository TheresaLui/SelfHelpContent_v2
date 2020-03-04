﻿<properties
	pageTitle="TSG Content Step: Check if on prem resources can reach resources in VNet with Gateway"
	description="TSG Content Step: Check if on prem resources can reach resources in VNet with Gateway"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public"
	articleId="ec701f16-bd9e-4dae-b66e-62772e6f5d87"
/>

# Check if on-premises client can reach resources in the Vnet that has the VPN gateway

A working site-to-site connection is necessary for the customer to reach resources in a spoke VNet connected to the VNet that has the VPN gateway. You need to eliminatte the site-to-site connection as a potential issue.

## **Recommended Steps**

1. From an on-premisespoint-to-site client, have the customer use ping, psping or tcpping, to try to communicate with a VM resource that is in the hub VNet where the VPN gateway is.


## **Recommended Documents**

* [Psping](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/171537/PsPing)

