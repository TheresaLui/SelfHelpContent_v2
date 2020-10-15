<properties
	pageTitle="Solution for VPN Point-to-Site error 0x576"
	description="Solution for VPN Point-to-Site error 0x576"
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
	articleId="cb096b65-093a-4096-972b-b4e5c300ecc5"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x576

The error *"0x576 => There is a time and/or date difference between the client and server"* is due to incorrect clock settings on the client device.

By design in the context of OpenVPN authentication via HMAC, the Azure VPN Gateway is checking the validity of the authentication timestamp sent by the client.
If the timestamp difference between client and server is bigger than -5 or +5 minutes, the authentication will fail with this error.

## Recommended Steps

1. Fix the client clock to be in sync with that of the Gateway (which takes the time from time.windows.com) by connecting it to a reliable time server.

## Recommended Documents

* [Time servers list](https://support.microsoft.com/help/262680/list-of-the-simple-network-time-protocol-sntp-time-servers-available)
