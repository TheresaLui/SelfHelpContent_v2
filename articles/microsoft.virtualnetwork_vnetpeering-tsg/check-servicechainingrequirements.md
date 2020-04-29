<properties
	pageTitle="TSG Content Step: Check Service Chaining Requirements"
	description="TSG Content Step: Check Service Chaining Requirements"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f163d69a-f684-42b2-ba4c-f08843da99d9"
	ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Check for service chaining requirements in a hub and spoke topology and complete configuration if needed

Service chaining in a hub and spoke topology requires the following:

* You must use a Network Virtual Appliance (NVA) in the Hub Vnet
* There must be UDRs in the spoke VNets with the next hop type of 'Network Virtual Appliance' pointing to the NVA
* NVA NICs must have *'IP Forwarding'* enabled
* NVAs must be configured correctly internally (requires NVA vendor assistance)

## **Recommended Steps**

1. Understand the customers topology. In ASC, go to Tools > 'Network Topology' to identify the spoke VNets and Hub VNet. 
2. Check to ensure the NVA has ***'IP Forwarding'*** enabled on the NICs

   1. Find the NVA VM in ASC > Resource Explorer
   2. In the VM properties check the property ***'Enable IP Forwarding'*** . It should be set to true. Correct if needed.
3. Check for UDRs in the spoke VNets

   1. Find a VM in each of the spoke VNets and do the following for each
   2. Find the VM in ASC > Resource Explorer
   3. Use TestTraffic to check for a UDR from this VM to a VM IP in the other spoke VNet <br>
          1. Specify the following options to Test Traffic and then click "Run":<br>
            * Traffic Direction: ***Out***<br>
            * Cluster node: Auto Populated by ASC<br>
            * Node Id: Auto Populated by ASC<br>
            * Container Id: Auto Populated by ASC<br>
            * Source IP: ***<client source IP address>***<br>
            * Source Port: 55555<br>
            * Destination IP: ***<Destination VM private VNet IP>***<br>
            * Destination Port: ***<choose port the customer is testing with: RDP=80; SSH=22; http=80; https=443)***<br>
            * Transport Protocol: TCP<br>
       2. Go to the ***'Stateless Test (Routing Layer)'*** section of the testtraffic result<br>
       3. Check the ***'Rule Name'*** field. It should be similar to "RouteTargetNVA_0"<br>
       4. Correct if needed according to the recommended documents below
   4. Also check the 'Stateful Test (NSG Layer)' for any blocking NSGs<br>
      1. If NSG is blocking remove the NSG<br>
4. Reverse the last two steps and check from the other VNet spoke 'out' to the spoke you just tested from
5. Use the ['Host-to-guest port scanner diagnostic'](https://aka.ms/vmportscanner) in ASC > Resource Explorer > VM > Diagnostics > Port Scan to validate the NVA is listening and responding on the correct port(s) (destination port(s).

## **Recommended Documents**

* [Service chaining](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview#service-chaining)

