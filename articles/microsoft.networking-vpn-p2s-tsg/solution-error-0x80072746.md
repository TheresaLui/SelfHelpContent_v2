<properties
	pageTitle="Solution for VPN Point-to-Site client error 0x80072746"
	description="Solution for VPN Point-to-Site client error 0x80072746"
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
	articleId="02f1b357-f685-4e84-a336-ec21c7c5efc9"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x80072746

The error *"Error 0x80072746: connection was forcibly closed by the remote host"* can happen if the windows client (often Windows 7 or Windows 8) does not have TLS 1.2 enabled in the OS.

## Recommended Steps

1. Enable TLS in Windows as outlined [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#tls1).

## Recommended Documents

* [Enabling TLS 1.2](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#tls1)
