<properties
	  pageTitle="Check virtual network conenctions to the HUB"
	  description="Check virtual network conenctions to the HUB"
	service="Microsoft.Network"
resource="Microsoft.network/virtualWans,Microsoft.Network/virtualwans,Microsoft.Network/virtualWans"
	  authors="lochiluk"
	  ms.author="Brwurz"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="21a7faac-8751-4902-ab55-7ce593e5b3d0"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Check virtual network connections to the HUB

In this step you'll be checking if the VNETs are connected to the hub. Please refer to the step below:

There are 3 different places to check those connections as below 
1) Look into the Virtual Network Connections section of HUB in ASC. 
2) Open the HUB VNET and look for peerings to the spoke VNETs. (Use this link on how to do so and refer to 3rd bullet point: https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/400028/VWAN-Routing-TS?anchor=required-information) 
3) Ask customer for spoke VNETs resource URI and open those VNETs and look for peering to HUB address space.

