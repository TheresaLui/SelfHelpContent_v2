<properties
	pageTitle="Azure Load Balancer backend pool connection issues"
	description="Azure Load Balancer backend pool connection issues"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6b"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer backend pool connection issues

## **Recommended Steps**
* If you are encountering SKU mismatch issues while assigning Public IP to the load balancer, make sure to upgrade both Public IP and load balancer to Standard SKU with the following steps.  
	1. Create a Standard Public IP address 
	2. Create a Standard Load balancer 
* If you are encountering SKU mismatch issues while adding virtual machines to the backend pool of a load balancer, make sure to upgrade both the Public IP of virtual machines and load balancer to Standard SKU with the following steps.
	1. Create a Standard Public IP address 
	2. Associate the Standard Public IP address to the network interface 
	3. Create a Standard Load balancer 
