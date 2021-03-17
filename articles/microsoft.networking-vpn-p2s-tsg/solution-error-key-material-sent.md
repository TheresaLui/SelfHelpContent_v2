<properties
	pageTitle="Error string Server did not respond properly to VPN control packets. Session state: Key Material Sent"
	description="Error string Server did not respond properly to VPN control packets. Session state: Key Material Sent"
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
	articleId="e523cd3d-7019-47f3-b49d-4c9e3b0c2606"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# [Needs Review] Solution for VPN Point-to-Site client Error string "Server did not respond properly to VPN control packets. Session state: Key Material Sent"

The error *"Server did not respond properly to VPN control packets. Session state: Key Material Sent"* is an Azure AD specific error where the VPN client app doesn't have the necessary rights on the Azure AD tenant. This issue occurs if the client is trying to connect with credentials that are incorrect or on a different AD tenant from that of the VPN Gateway is utilizing. Follow the steps below to validate the client app has the necessary rights on Azure AD.

## Recommended Steps

1. Check the username/password combination on the Azure VPN Client [Needs Review: Where?]
2. If credentials are correct, the credential token was granted but not accepted by the Server, which means that Server is configured with different AAD Settings. 
   1. Connect with a user that belongs to the same Azure AD tenant that has been configured for this Gateway.
   2. Normally the error can happen if another tenant is used, that is also configured for Azure VPN, for but another Gateway.

## Recommended Documents

* [Create an Azure Active Directory tenant for P2S OpenVPN protocol connections](https://docs.microsoft.com/en-us/azure/vpn-gateway/openvpn-azure-ad-tenant)
