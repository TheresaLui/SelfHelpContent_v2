<properties
	pageTitle="Check if Floating IP is enabled on the backend resources"
	description="Check if Floating IP is enabled on the backend resources"
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
	articleId="351e248d-0f4c-4cfe-be02-3a1f8c4879a3"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check if Floating IP is enabled on the backend resources

## **Recommended Steps**

* Find the Load Balancer in Resource Explorer in Azure Support Center
* Find the load balancing rules used for the customer solution and expand
* Check the property "Enable Floating IP"

For more information on Floating IPs check this Microsoft Docs Resource below

## **Recommended Documents**

* [backend port reuse by using Floating IP](https://docs.microsoft.com/azure/load-balancer/load-balancer-multivip-overview#rule-type-2-backend-port-reuse-by-using-floating-ip)
