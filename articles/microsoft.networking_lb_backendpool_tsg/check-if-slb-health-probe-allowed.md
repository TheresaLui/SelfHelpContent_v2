<properties
	pageTitle="Check if SLB Health Probe is Allowed"
	description="Check if SLB Health Probe is Allowed"
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
	articleId="1a1c538b-332e-401b-84e1-e1c1f7ed2456"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check if SLB Health Probe is Allowed

## Description

Check if SLB Health Probe is Allowed in a NSG. In order for a load balanced endpoint to be accessible to clients, at least one member of the backend pool must pass the customer configured health probe. If the health probe does not pass, it may be due to a NSG blocking access to the health probe source IP 168.63.129.16. Use these steps to determine if that is the case.

## **Recommended Steps**

* In Azure Support Center, browse to the load balancer object and browse to the Load Balancing Rules section
* Find the load balanced rule for the front end port the customer reported issues with and expand that tab. Make note of the probe name.
* Scroll down to the "Probes" header and find the configuration name of the probe found in step 2. Make note of the protocol and port the customer configured.
* Next, browse to the backend pool member Virtual Machine in ASC Resource Explorer. Click on the Diagnostics tab, and choose Test Traffic.
* Specify the following options to Test Traffic and then click "Run":
   * Traffic Direction: Internet In
   * Cluster node: Auto Populated by ASC
   * Node Id: Auto Populated by ASC
   * Container Id: Auto Populated by ASC
   * Source IP: 168.63.129.16
   * Source Port: 1067
   * Destination IP: VM DIP
   * Destination Port: Use the value from Step 3 above, if probe protocol is HTTP use 80, if probe protocol is HTTPS use 443
   * Transport Protocol: TCP
* Ensure that the overall result is Allowed
