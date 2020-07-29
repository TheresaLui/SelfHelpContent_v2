<properties
	pageTitle="Error 3399942148"
	description="Error 3399942148"
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
	articleId="0db3e0eb-81d2-4917-ac8e-704509ce487b"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>


# Solution for VPN Point-to-Site client Error 3399942148

The error *"Error 3399942148: Failure in Acquiring AAD TokenProvider. The server or Proxy was not found"* is an Azure AD specific error where the VPN client app isn't able to connect to Azure Active Directory.

## Recommended Steps

Running the [Diagnostics operation](https://docs.microsoft.com/en-us/azure/vpn-gateway/troubleshoot-ad-vpn-client) in the VPN Profile will help understanding this issue.

1. Validate if the client machine has internet access
2. Validate if customer's firewall or Proxy does not block access to the AAD Endpoint https://login.microsoftonline.com

## Recommended Documents

* https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-tenant
* https://docs.microsoft.com/en-us/azure/vpn-gateway/troubleshoot-ad-vpn-client

