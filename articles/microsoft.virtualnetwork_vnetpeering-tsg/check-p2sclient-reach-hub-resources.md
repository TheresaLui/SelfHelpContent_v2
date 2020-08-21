<properties
	pageTitle="TSG Content Step: check if p2s client can reach resources in Vnet with gateway"
	description="TSG Content Step: check if p2s client can reach resources in Vnet with gateway"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3c50a598-87d9-45de-b2af-132c4c40de55"
/>

# Check if p2s client can reach resources in the Vnet that has the VPN gateway

A working point-to-site connection is necessary for the customer to reach resources in a spoke VNet connected to the VNet that has the VPN gateway. You need to eliminatte the point-to-site connection as a potential issue.

## **Recommended Steps**

1. From the point-to-site client, have the customer use ping, psping or tcpping, to try to communicate with a VM resource that is in the hub VNet where the VPN gateway is.


## **Recommended Documents**

* [Psping](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/171537/PsPing)




