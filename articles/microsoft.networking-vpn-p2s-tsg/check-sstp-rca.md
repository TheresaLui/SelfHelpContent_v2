<properties
	pageTitle="Check SSTP RCA"
	description="Check SSTP RCA"
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
	articleId="df5103e7-f37d-4f9e-be7a-ab1dcdb9a3ef"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if the customer was using SSTP protocol at the time of the issue

## Recommended Steps  

1. Go to ASC > Resource Explorer and select the VPN gateway
2. Check the **VPN Tunneling Protocols** property
3. If the customer has more than one protocols enabled (for example SSTP + IKEv2) the only way to tell whether the failing client was using SSTP or IKEv2 is to ask the customer.

**Note**: the customer might have changed the setting since the time of the issue. It is advised to doublecheck with customer.
