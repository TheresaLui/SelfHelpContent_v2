<properties
	pageTitle="Check whether there is an NSG on the gateway subnet"
	description="Check whether there is an NSG on the gateway subnet"
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
	articleId="bfffa3c0-fb07-4a00-8341-3885edb8d7d8"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# How to check whether there is an NSG on the gateway subnet

## **Recommended Steps**

* NSG and UDR can affect the control plane operations between Gateway Manger and Gateway Tenants
* This may also result in Gateway going to failed state which will block any new operations. This can also affect other resources like Connections, Local Network Gateway going into failed state.  
* ASC has an insight that will flag if an NSG is applied on the VPN Gateway subnet


## **Recommended Documents**

* [Virtual Network UDR Overview](https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview#default-route)
