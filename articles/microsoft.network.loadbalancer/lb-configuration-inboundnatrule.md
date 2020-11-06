<properties
	pageTitle="Azure Load Balancer Configuration Issues - Inbound NAT Rules"
	description="Azure Load Balancer Configuration Issues - Inbound NAT Rules"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781312"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6j"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer Inbound Nat Rules Set Up

## **Recommended Steps**

* Inbound NAT rules let you configure port forwarding for individual virtual machines in the backend of a load balancer. Learn more about [inbound NAT rules](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal).
* Learn more about [how to create an inbound NAT rule](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal#create-an-inbound-nat-port-forwarding-rule) 
* Understand when to use inbound NAT rules versus [load balancing rules](https://docs.microsoft.com/azure/load-balancer/components#load-balancing-rules). 
  1. To forward traffic from a specific port of the front end IP address to a specific port of a backend VM, use inbound NAT rules. 
  2. To load balance traffic to all instances within the backend pool, use load balancing rules. A load balancing rule maps a specific frontend IP configuration and port to multiple backend IP address and ports. 
