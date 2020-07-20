<properties
pageTitle="Solution update point-to-site client routes"
description="Solution update point-to-site client routes"
infoBubbleText="Solution update point-to-site client routes"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionUpdateP2SClientRoutes"
diagnosticScenario="SolutionUpdateP2SClientRoutes"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Routes missing on point-to-site client

The issue was due to the point-to-site clients not having new VNet routes. Anytime there is a change in a VNet's IP ranges, such as adding a peered VNet, the point-to-site client routes must be updated to include the new routes either via the package being redownloaded/redeployed or VPN gateway must be set to use BGP or finally the routes must be added manually to the client.

## **Recommended Steps**

1. [Create and install VPN client configuration files](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-vpn-client-configuration-azure-cert) or
2. [Configure BGP on Azure VPN Gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps)

## **Recommended Documents**

* [Point-to-Site client configuration](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-vpn-client-configuration-azure-cert)
* [How to configure BGP on Azure VPN Gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps)
