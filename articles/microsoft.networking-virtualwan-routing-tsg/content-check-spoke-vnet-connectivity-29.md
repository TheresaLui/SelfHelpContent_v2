<properties
	  pageTitle="Check Spoke VNET connectivity"
	  description="Check Spoke VNET connectivity"
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
	  articleId="304f48bf-bdd0-4b36-bdcd-4a8ac257b5cf"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Check Spoke VNET connectivity

In this step you'll be checking if the VNETs are connected to the hub. Please refer to the step below:

There are 3 different places to check those connections as below 
1) Please look into the Virtual Network Connections section of HUB in ASC. 
2) Please open the HUB VNET and look for peerings to the spoke VNETs. (Use this link on how to do so and refer to 3rd bullet point: https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/400028/VWAN-Routing-TS?anchor=required-information) 
3) ask customer for spoke VNETs resource URI and open those VNETs and look for peering to HUB address space.

