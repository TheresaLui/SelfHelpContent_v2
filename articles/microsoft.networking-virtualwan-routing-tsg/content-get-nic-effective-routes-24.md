<properties
	  pageTitle="Get NIC effective routes"
	  description="Get NIC effective routes"
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
	  articleId="6bee95b2-b1aa-4270-9a5d-fc2f2be77104"
	  ownershipId="Cloudnet_VirtualWAN"
/>

# Get NIC effective routes

In this step, you'll have to pull up a virtual machine from the spoke VNET you're having issues with and get the NIC effective routes. Please use the steps below:

1) Open a VM in the spoke VNET in ASC (Any VM should work which is in running state) 
2) Navigate to Diagnostics tab on ASC 
3) Run a test traffic from VM IP as source to destination IP address on port customer wants to connect on or for just testing you can use port 80 as destination port. 
4) Open child VPN gateway and in the Brooklyn gateway properties section, click on the raw data URI and open it with notepad. 
5) Search for CAs and find the instance private IPs (which are CAs) 
6) Now, Look at the effective routes and find the destination address space and see if you can see the next hop type virtual network gateway pointing to VPN gateway CA address. Note: Traffic do not hit route service in this scenario.

