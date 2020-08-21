<properties
	pageTitle="Disable or correct the Floating IP configuration"
	description="Disable or correct the Floating IP configuration"
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
	articleId="7b551c23-e9e1-45c6-a56c-8d888db664c5"
	ownershipId="CloudNet_LoadBalancer"
/>

# Disable or correct the Floating IP configuration

* Determine if the customer’s Virtual Machine has a loopback adapter or cluster resource with the IP address of the frontend IP associated with the load balancing rule.  
* If the customer is not using clustering, doesn’t know what a loopback adapter is, or doesn’t know what the "Floating IP (direct server return)" setting is, they should probably disable it.  
* However, if the customer wants the setting enabled:
   * If the customer is using a Windows Cluster solution (most often as part of a SQL AlwaysOn deployment), have the customer connect to the primary member of the Windows Cluster run the command ipconfig and ensure the load balancer frontend IP is listed in the output under the Ethernet interface.
   * If the customer is not using a clustering technology, validate the customer has a loopback adapter configured in their guest OS.  Run the command ipconfig (Windows) or ip addr (Linux).  Ensure the load balancer frontend IP is listed in the output under the Ethernet interfaces listed (Windows) or eth#/lo interface (Linux).
