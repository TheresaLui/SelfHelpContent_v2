<properties
	pageTitle="Not Supported (Windows Version)"
	description="Not Supported (Windows Version)"
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
	articleId="f2808964-b31e-4f2b-b7c5-a14168111d2b"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Windows Version not supported

We found the cause of the issue was due to the point-to-site client Windows version being out of support. 

## Recommended Steps

1. Update the clients to Windows 10
2. Install all required hotfixes and registry settings

## Recommended Documents

* [Supported Windows 10 Versions](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#does-azure-support-ikev2-vpn-with-windows)