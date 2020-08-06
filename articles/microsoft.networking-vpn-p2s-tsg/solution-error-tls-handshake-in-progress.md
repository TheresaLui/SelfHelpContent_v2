<properties
	pageTitle="Error string Server did not respond properly to VPN control packets. Session state: TLS Handshake in Progress"
	description="Error string Server did not respond properly to VPN control packets. Session state: TLS Handshake in Progress"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="crcritel,stegag"
	ms.author="crcritel,stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="8ff50259-e147-4b23-ae44-ef462e5da24a"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for Error "...Session state: TLS Handshake in Progress"

The error *"Server did not respond properly to VPN control packets. Session state: TLS Handshake in Progress"* is an Azure AD specific error where the VPN client certificate is incorrect. Follow the steps below to validate the certificate.

## Recommended Steps [Need Validation]

1. If the Server Stops responding in the TLS Handshake phase, please check the Client Cert is acceptable to the server.
(how???) 

## Recommended Documents

* [Create-and-install-client-certificates](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert#create-and-install-client-certificates)
