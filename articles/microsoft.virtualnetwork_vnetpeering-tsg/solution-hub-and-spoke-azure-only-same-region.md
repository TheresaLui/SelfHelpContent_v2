<properties
pageTitle="SolutionHubAndSpokeAzureOnlySameRegion"
description="SolutionHubAndSpokeAzureOnlySameRegion"
infoBubbleText="SolutionHubAndSpokeAzureOnlySameRegion"
service="microsoft.network"
ownershipid="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionHubAndSpokeAzureOnlySameRegion"
diagnosticScenario="SolutionHubAndSpokeAzureOnlySameRegion"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, fairfax, usnat, ussec"
/>
# Check for service chaining requirements in a hub and spoke topology
<!--issueDescription-->

From our interaction, it appears you are looking for steps on how to setup VNet peering between VNet spokes in a hub-and-spoke topology. To accomplish this you must use 'Service chaining'. A hub and spoke topology requires the following:

* You must use a Network Virtual Appliance (NVA) in the Hub Vnet
* There must be UDRs in the spoke VNets with the next hop type of 'Network Virtual Appliance' pointing to the NVA
* NVA NICs must have *'IP Forwarding'* enabled
* NVAs must be configured correctly internally (requires NVA vendor assistance)

<!--/issueDescription-->

## **Recommended Steps**

* Please follow step by step 'Service chaining' instructions in the recommended documents below

## **Recommended Documents**

* [Service chaining](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview#service-chaining)
* [Troubleshooting Network Virtual Appliances](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)


