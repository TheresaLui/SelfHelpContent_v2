<properties
	pageTitle="My load balanced VMs are not receiving traffic"
	description="Troubleshoot connectivity issues to the load balanced virtual machines in your virtual network"
	service="microsoft.network"
	resource="loadbalancers"
	authors="radwiv"
	ms.author="radwiv"
	category="Connectivity"
	searchTags=""
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8ae1e668-23e1-42d7-8e23-5fb74f1962e7"
	ownershipId="CloudNet_LoadBalancer"
/>

# My load balanced VMs are not receiving traffic

## **Recommended Steps**

If you have configured Load Balancer in your virtual network and have connectivity issues, try one or more of the below steps to resolve the issue.<br>

1. Check if the Virtual Machines in the Load Balancer's Backend Pool are responding to Load Balancer Probe:

	* Check if the Virtual Machines are up and available
	* Check if the Virtual Machines are listening on the probe port
	* Check if the Network Security Groups on load balancer backend pool VM allow traffic on probe port

2. Check if the Virtual Machines in the Load Balancer's Backend Pool are receiving and responding to traffic on data port:

	* Check if the Virtual Machines are listening on the data port
	* Check if the Network Security Groups on load balancer backend pool VM allow traffic on data port
	* Check if a participating VM from backend pool is not trying to access the Internal Load Balancer VIP

## **Recommended Documents**

* [Troubleshoot Azure Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-troubleshoot)
