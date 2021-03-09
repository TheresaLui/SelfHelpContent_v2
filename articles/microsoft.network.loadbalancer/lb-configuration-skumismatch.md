<properties
	pageTitle="Azure Load Balancer Configuration issues - SKU Mismatch"
	description="Azure Load Balancer Configuration issues - SKU Mismatch"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781317"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6h"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer SKU Mismatch problem

## **Recommended Steps**

1. If you are encountering SKU mismatch issues while assigning Public IP to the load balancer, make sure to upgrade both Public IP and load balancer to Standard SKU with the following steps: 
   - [Create a Standard Public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address#create-a-public-ip-address)
   - [Create a Standard Load balancer](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard)
* If you are encountering SKU mismatch issues while adding virtual machines to the backend pool of a load balancer, make sure to upgrade both the Public IP of virtual machines and load balancer to Standard SKU with the following steps:
   - [Create a Standard Public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address#create-a-public-ip-address)
   - [Associate the Standard Public IP address to the network interface](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-addresses#add-ip-addresses) 
   - [Create a Standard Load balancer](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard)
