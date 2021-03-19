<properties
	pageTitle="TSG Content Step: Check platform nsg and routing from source 'DirectionOut'"
	description="TSG Content Step: Check platform nsg & routing from source 'DirectionOut'"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="fc893080-ae65-4691-bab3-33a1bb2cb08e"
        ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# Check Azure platform nsg and routing from source to destination

Use the 'Test Traffic' utility to check for blocking Network Security Group Rules (NSGs) and Routing Rules **leaving the source** toward the destination.

## **Recommended Steps**

1. Choose a 'source' VM or VMSS instance in one of the peered VNet and a 'destination' VM in the other peered VNet. (For the next several steps we will refer to the VMs you've selected as 'source' & 'destination' VM)
2. Browse to the source VM/VMSS instance in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
3. Specify the following options to Test Traffic and then click "Run":
   * Traffic Direction: ***Out***
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: client source IP address (Auto Populated by ASC)
   * Source Port: ***55555***
   * Destination IP: ***<'enter destination VM private VNet IP>***
   * Destination Port: ***<'enter port the customer is testing with>***
   * Transport Protocol: ***TCP***
4. Make note of the following: 
   * The 'Test Result' for the "Stateful Test (NSG Layer)" and the blocking Rule Name listed.
   * The "Stateless Test (Routing Layer)" any 'NSG or Routing Layer' and the blocking Rule Name listed.

## **Recommended Documents**

1. [TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)
