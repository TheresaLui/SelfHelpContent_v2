<properties
	pageTitle="Check if source traffic is allowed to backend pool members"
	description="Check if source traffic is allowed to backend pool members"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="76f8bcf5-a452-4332-b3db-016d0b692037"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check if source traffic is allowed to backend pool members

## Description

Check if source address/port is allowed or blocked by a NSG. In order for backend pool resources to be accessible to clients, at least one member of the backend pool must have an NSG that *Allows* traffic from the source IP and port. Use these steps to validate if traffic can flow from source to backend pool without NSGs blocking.

## **Recommended Steps**

1. In Azure Support Center, browse to the load balancer object and browse to the Load Balancing Rules section
2. Find the load balanced rule for the front end port the customer reported issues with and expand that tab.
3. Make note of the protocol and port the customer configured.
4. Next, browse to the backend pool member Virtual Machine in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
5. Specify the following options to Test Traffic and then click "Run":
   * Traffic Direction: Internet In
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: client source IP address
   * Source Port: 1067
   * Destination IP: VM DIP
   * Destination Port: Use the value from Step 3 above, if probe protocol is HTTP use 80, if probe protocol is HTTPS use 443
   * Transport Protocol: TCP
6. Ensure that the overall result is Allowed
