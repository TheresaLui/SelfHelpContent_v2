<properties
	pageTitle="Check if source traffic is allowed to backend pool members"
	description="Check if source traffic is allowed to backend pool members"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber,mariliu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="76f8bcf5-a452-4332-b3db-016d0b692037"
	ownershipId="CloudNet_LoadBalancer"
/>

# Inbound direction: How to check if source traffic is allowed to backend pool members

## **Description**

Use the 'Test Traffic' utility to check both below:

1. If source address/port is allowed or blocked by Network Security Group Rules (NSGs)
2. If there's any unusual Routing Rules (UDR) from source coming into the destination backend pool resources

In order for backend pool resources to be accessible to clients, at least one member of the backend pool must have an NSG that *Allows* traffic from the source IP and port. Use these steps to validate if traffic can flow from source to backend pool without NSGs and/or UDR blocking. 

## **Recommended Steps**

1. In Azure Support Center, browse to the load balancer object and browse to the Load Balancing Rules section
2. Find the load balanced rule for the front end port the customer reported issues with and expand that tab
3. Make note of the protocol and port the customer configured
4. Next, browse to the backend pool member Virtual Machine in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
5. Specify the following options to Test Traffic and then click "Run":

   * Traffic Direction: ***Internet In***
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: ***client source IP address*** 
   * Source Port: ***5555***
   * Destination IP: VM DIP
   * Destination Port: ***Use the value from Step 3 above***
   * Transport Protocol: TCP

6. Ensure that the overall result is **Allowed**. If not, make note of the following and address them:
   
   * The 'Test Result' for the "Stateful Test (NSG Layer)" and the blocking Rule Name listed
   * The "Stateless Test (Routing Layer)" and the blocking Rule Name listed

## **Recommended Documents**

* [ASC: TestTraffic](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/133274/ASC-TestTraffic)
