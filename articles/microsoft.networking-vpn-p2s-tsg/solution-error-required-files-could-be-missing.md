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

Most users can resolve this issue by reconfiguring the gateway, and downloading and installing the updated VPN P2S client package again.

## Recommended Steps

1. From the Azure portal, select the impacted VPN gateway.
2. On the **Point-to-site configuration** page, configure the Tunnel type as SSTP only.
3. Select **Save** and wait for changes to apply.
4. Reconfigure the Tunnel type as it was previously, according to what the customer wants.
5. Select **Save** and wait for the changes to apply again.
6. Download the package again from the portal and reinstall the package on all clients.

## Recommended Documents

* [VPN Gateway point-to-site resource manager](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-how-to-point-to-site-resource-manager-portal)
