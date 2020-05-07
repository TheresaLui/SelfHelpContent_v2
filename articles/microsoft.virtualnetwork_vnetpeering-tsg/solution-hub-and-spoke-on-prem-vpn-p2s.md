<properties 
pageTitle="SolutionHubAndSpokeOnpremVpnP2s"
description="SolutionHubAndSpokeOnpremVpnP2s"
infoBubbleText="SolutionHubAndSpokeOnpremVpnP2s"
service="microsoft.network"
ownershipid="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionHubAndSpokeOnpremVpnP2s"
diagnosticScenario="SolutionHubAndSpokeOnpremVpnP2s"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, fairfax, usnat, ussec"
/>

# Step by step for connecting VNet Peering spokes to point-to-site VPN clients
<!--issueDescription-->

From our interaction, it appears you are looking for steps on how to setup VNet peering between a VNet and point-to-site VPN clients.

<!--/issueDescription-->

## **Recommended Steps**

If your point-to-site clients cannot connect with resources in a remote vnet that is peered with the point-to-site VPN Vnet, ensure the following:
1. Steps for regular VPN site-to-site are correct
	
	1. The 'use remote gateway' option is selected for the spoke Vnet that doesn't have a VPN gateway. (You will not be able to enable this if your spoke Vnet has a gateway by-design)
	2. The 'allow gateway transit' option must be enabled on the hub Vnet that has the point-to-site VPN gateway.
	3. The point-to-site package must be downloaded and ***installed again AFTER*** Vnet Peering has been established or changed for the point-to-site package to have the updated routes.

