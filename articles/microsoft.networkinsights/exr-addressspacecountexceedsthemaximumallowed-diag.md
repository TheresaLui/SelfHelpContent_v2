<properties
pageTitle="Address Space Prefix Count Exceeds The Maximum Allowed"
description="Address Space Prefix Count Exceeds The Maximum Allowed"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors=""
displayOrder="10"
articleId="ExRVnetAddressSpacePrefixCountExceedsTheMaximumAllowedInsight"
diagnosticScenario="ExRVnetAddressSpacePrefixCountExceedsTheMaximumAllowedInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# ExpressRoute Address Prefix Count Exceeded
<!--issueDescription-->
We have identified your private peering ExpressRoute connection to virtual network ID: **<!--$VNetId-->[VNetId]<!--/$VNetId-->** has exceeded the maximum allowed prefix count of 200 from the virtual network. This can result in connectivity issues to some IP address prefix ranges.
<!--/issueDescription-->
## **Steps to resolve this issue**
 Please reduce the VNet address space count to less than 200 prefixes for VNetId: **<!--$VNetId-->[VNetId]<!--/$VNetId-->**. You may refer to the following document for steps on managing your VNet settings: [Change subnet settings](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet#change-subnet-settings).
