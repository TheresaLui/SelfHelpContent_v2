﻿<properties
	pageTitle="TSG Content Step: Check platform nsg & routing to destination 'DirectionIn'"
	description="TSG Content Step: Check platform nsg & routing to destination 'DirectionIn'"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public"
	articleId="39659e63-a65c-46b5-8f87-7d1d43da1739"
ownershipId="ASEP_ContentService_Placeholder"
/>
# Check Azure platform nsg & routing from source to destination

Use the 'Test Traffic' utility to check for blocking Network Security Group Rules (NSGs) and Routing Rules from source coming **into the destination** VM. (You will leverage the same 'source' and 'destination' VMs as in the previous step. The VMs you labeled as 'source' and 'destination' will maintain that designation for this step)

## **Recommended Steps**

1. Browse to the destination VM in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
2. Specify the following options to Test Traffic and then click "Run":

   * Traffic Direction: ***TunnelOrLocalIn***
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: ***<'Source' private IP address>***
   * Source Port: 55555
   * Destination IP: ***<'Destination' private IP address>***
   * Destination Port: ***<'choose port the customer is testing with: RDP=80; SSH=22; http=80; https=443>***
   * Transport Protocol: TCP
4. Make note of the following: 

   * The 'Test Result' for the "Stateful Test (NSG Layer)" and the blocking Rule Name listed.
   * The "Stateless Test (Routing Layer)" any 'NSG or Routing Layer' and the blocking Rule Name listed.

## **Recommended Documents**

* [TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)


