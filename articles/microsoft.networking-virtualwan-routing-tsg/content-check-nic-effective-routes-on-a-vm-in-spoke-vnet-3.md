<properties
	  pageTitle="Check NIC effective routes on a VM in Spoke VNET"
	  description="Check NIC effective routes on a VM in Spoke VNET"
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
	  articleId="76d3a227-ab30-40f7-87b8-91831523c818"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Check NIC effective routes on a VM in Spoke VNET

In this step, you'll have to pull up a virtual machine from the spoke VNET you're having issues with and get the NIC effective routes. Please use the steps below:

1) Open a VM in the spoke VNET in ASC (Any VM should work which is in running state) 
2) Navigate to Diagnostics tab on ASC 
3) Run a test traffic from VM IP as source to destination IP address on port customer wants to connect on or for just testing you can use port 80 as destination port. 
4) Look at the effective routes and find the destination address space and see if you can see the next hop type virtual network gateway pointing to Route service VIP. 

Note: you can find the Route service VIP in get Route service section of HUB ASC.

