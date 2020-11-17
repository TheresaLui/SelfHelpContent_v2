<properties
	  pageTitle="Run scenario using Test Traffic Tool"
	  description="Run scenario using Test Traffic Tool"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="84ed4c9e-16d1-4094-9cb1-73b4aba1e7b3"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Run scenario using Test Traffic Tool

TestTraffic is a feature of Azure Support Center that takes IP and port parameters to run against stateful (NSG) and stateless (UDR) VFP rules on the platform, if traffic theoretically is allowed or blocked.

Make sure that you take note of the NSGs and Route Tables/UDRs attached to both VMs from the results of running TestTraffic tool.

## Recommended Steps

1. Navigate to the destination VM in ASC Resource Explorer
2. Select the Diagnostics tab
3. Select **TestTraffic**
4. Fill out the required boxes for inbound. (Highlight the **i** icon for tips if you are unsure of any box)
5. Click **Run** for results
6. Review results to determine if traffic is allowed or blocked
7. Navigate to the source VM in ASC Resource Explorer
8. Select the Diagnostics tab
9. Select **TestTraffic**
10. Fill out the required boxes for outbound traffic. (Highlight **i** icon for tips if you are unsure of any box)
11. Click **Run** for results
12. Review results to determine if traffic is allowed or blocked

## Reccommended Documents

1. [ASC TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)

