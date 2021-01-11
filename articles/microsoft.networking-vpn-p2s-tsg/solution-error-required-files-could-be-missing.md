<properties
	pageTitle="Solution for VPN Point-to-Site client error Required files could be missing"
	description="Solution for VPN Point-to-Site client error Required files could be missing"
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
	articleId="897ae4f5-51be-428c-abce-3243c7cca50c"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error Required files could be missing

Thank you for working with us to identify the cause of the issue you are experiencing. The solution to this issue is to reconfigure the gateway and download and install the updated VPN P2S client package again.

We believe this has met your need but feel free to reach out for assistance if needed. We are sorry for the inconvenience. If you have thoughts on how we can improve we would appreciate any feedback you can offer.

## Recommended Steps

1. From The Azure Portal, select the impacted VPN gateway.
2. On the **Point-to-site configuration** page configure the Tunnel Type as SSTP only.
3. Hit **Save** and wait for changes to apply.
4. Reconfigure Tunnel type as it was previously, per customer desire.
5. Hit **Save** and wait for changes to apply again.
6. Redownload package from portal and re-install on all clients.

## Recommended Documents

* https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal
