<properties
	pageTitle="TSG Content Step: Check connectivity by bypassing blocking NSG"
	description="TSG Content Step: Check connectivity by bypassing blocking NSG"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3767257a-9a49-42fb-8856-8e0c3bee0668"
        ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Check connectivity again after bypassing the blocking NSG

* By default, VMs in the same virtual network and peered virtual network can communicate with one another due to a system routing rule allowing intra Virtual Network connectivity. More information in online docs [Virtual network traffic routing](https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview). Any NSGs blocking intra Vnet connectivity will typically be intentional and for customer's security compliance reasons.
* Understand the customer environment and purpose for the blocking NSG
* Talk to the customer about the purpose of that particular NSG and its attributes (src IP, dest IP, port, blocked vs allowed) to demonstrate interest in the customer's environment and understand the bigger picture with the customer.

## **Recommended Steps**

1. Note the NSG details and remove the blocking NSG or
2. Create an allow rule with a higher priority (lower number)
3. Run TestTraffic again as in the previous step and/or have the customer test

## **Recommended Documents**

1. [TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)


