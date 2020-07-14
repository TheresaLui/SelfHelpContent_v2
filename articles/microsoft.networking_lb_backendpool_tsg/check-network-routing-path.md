<properties
	pageTitle="Check network routing path from backend pool VM to client"
	description="Check network routing path from backend pool VM to client"
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
	articleId="8eb9c6b5-1a36-4273-8c35-1cf0819c510b"
	ownershipId="CloudNet_LoadBalancer"
/>

# Outbound: How to check network routing path from backend pool VM to client

## **Recommended Steps**

* Browse to the backend pool member Virtual Machine in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
* Specify the following options to Test Traffic and then click "Run":
   * Traffic Direction: Outbound
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: ***BE VM DIP***
   * Source Port: ***5555***
   * Destination IP: client IP accessing the LB solution
   * Destination Port: ***5555***
   * Transport Protocol: TCP

**IMPORTANT:**

For this check, you are only looking at the **Rule Name** value in 'Stateless Test (Routing Layer)'. *The Test Traffic results of the 'Routing Layer Rule Name'* MUST BE "RouteTargetInternet_0".

**More information:**

* If the Routing rule name result is "RouteTargetNVA_0" or "RouteTargetVPNGateway_0" the LB solution will NOT work.
* UDRs are typically a network security compliance requirement.
* If customer is not the network administrator they should check with their network administrator to see how they wish to proceed.

