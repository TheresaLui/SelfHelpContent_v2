<properties
	pageTitle="Not Supported - RCA for SSTP"
	description="Not Supported - RCA for SSTP"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="0fee49bc-cc68-4dff-959b-74912e305bdf"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for RCA for SSTP clients is not possible

Due to the Design of the VPN Gateway, the SSTP protocol is serviced by the Windows RRAS server role. Such component does not have always on logging - hence it is not possible to RCA past issues with detail. 

IKEv2 and OpenVPN protocols instead are handled by an Azure Specific driver on the Gateway, which has always on logging to Jarvis/Kusto enabled by default as well as other benefits, such as, better scalability.

## Recommended Steps:

1. For always on logging use IKEv2 or OpenVPN protocols 


## Recommended Documents

* [About Gateway SKUs](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku)

