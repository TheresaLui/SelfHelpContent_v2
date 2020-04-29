<properties
	pageTitle="TSG Content Step: Check bypassing the blocking routing rules"
	description="TSG Content Step: Check bypassing the blocking routing rules"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="cedce745-1dcb-4878-95e6-a15d33633607"
        ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Check bypassing the blocking routing rules

By default, VMs in the same virtual network and peered virtual network can communicate with one another due to a system routing rule allowing intra Virtual Network connectivity. User-defined routes (UDRs) can be introduced overriding the system intra Vnet routes. UDRs will typically be intentional and for customer's security compliance reasons.

Understand the customer environment and purpose for the UDR. Talk to the customer about the purpose of that particular UDR and its attributes (src IP, next hop) to demonstrate interest in the customer's environment and understand the bigger picture with the customer.

## **Recommended Steps**

1. Have customer Open the Azure portal
2. Find the VM you ran TestTraffic against, select the 'Networking' tab and click on the link for the 'Network Interface'
3. In the NIC resource select the 'Effective Routes' tab
4. Note the effective routes where the 'source' = User
5. Click on the Associated Route Table link
6. Make note of the blocking UDR properties so it can be recreated in a later step if necessary
7. Delete the UDR **or** create a new UDR for the VM with a /32 address prefix with next hop Virtual Network
8. Have customer test connectivity (you can also run Test Traffic again and repeat these steps until traffic is allowed)
   

***Note: It is possible the customer will not want to bypass their UDR. Assure and stress to the customer that this is a necessary step and is just for a 5-10 minute step to rule out the UDR as causing the issue.***

## **Recommended Documents**

* [TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)


