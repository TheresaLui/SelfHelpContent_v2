<properties
	pageTitle="Guidelines (MAC Ikev2)"
	description="Guidelines (MAC Ikev2)"
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
	articleId="aab1db29-b8ae-40c7-8598-8eca0cf00bdf"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check guidelines for MAC IKEv2 clients

When troubleshooting Point to Site issue with Mac clients, the customer needs to understand that our support is limited.
We can only debug the Gateway side, and if we determine that the issue is on the client side, we might need to ask the customer that he engages Apple support. The steps below are the ***requirements*** for MAC OS X clients.

## Recommended Steps

1. Check if customer **Mac OS X client is running version 10.11 or above.** (It is always recommended for customer to run the latest OS version if possible)
2. Have customer follow the [Mac Install for Point to Site IKE v2](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-vpn-client-configuration-azure-cert#installmac) document for proper installation of clients.
3. Have customer manually [configure the native IKEv2 VPN client](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-vpn-client-configuration-radius#admaccli
) on every Mac that will connect to Azure. Azure does not provide mobileconfig file for native Azure certificate authentication.
