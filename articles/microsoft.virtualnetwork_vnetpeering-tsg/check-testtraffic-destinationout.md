<properties
	pageTitle="TSG Content Step: Check platform nsg and routing from destination to source 'TrafficDirectionOut'"
	description="TSG Content Step: Check platform nsg and routing from destination to source 'TrafficDirectionOut'"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="448c12c5-1e26-45d4-b9b6-c707e4e7ecb5"
        ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# Check Azure platform nsg and routing from destination to source

Use the 'Test Traffic' utility to check for blocking Network Security Group Rules (NSGs) and Routing Rules **leaving the destination** out to the source VM or VMSS instance. (You will leverage the same 'source' and 'destination' VM/VMSS as in the previous step. The VM/VMSS you labeled as 'source' and 'destination' will maintain that designation for this step)

## **Recommended Steps**

1. Browse to the destination VM/VMSS in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
2. Specify the following options to Test Traffic and then click "Run":
   * Traffic Direction: ***Out***
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: ***<'Destination' private IP address>***
   * Source Port: ***55555***
   * Destination IP: ***<'Source' private IP address>***
   * Destination Port: ***<'choose port the customer is testing with'>***
   * Transport Protocol: ***TCP***
4. Make note of the following: 
   * The 'Test Result' for the "Stateful Test (NSG Layer)" and the blocking rule name listed.
   * The "Stateless Test (Routing Layer)" any 'NSG or Routing Layer' and the blocking rule name listed.

## **Recommended Documents**

* [TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)

