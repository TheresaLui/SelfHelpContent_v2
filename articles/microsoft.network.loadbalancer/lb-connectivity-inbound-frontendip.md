<properties
	pageTitle="Azure Load Balancer Connectivity Issues - Cannot connet to a Frontend IP Address"
	description="Azure Load Balancer Connectivity Issues - Cannot connect to a Frontend IP Address"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781320"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6g"
	ownershipId="CloudNet_LoadBalancer"
/>

# No inbound connectivity to frontend IP of Azure Load Balancer

## **Recommended Steps**
* [Load balancing rule](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard#create-a-load-balancer-rule) or [inbound NAT rule](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-port-forwarding-portal) is required to establish inbound connection. Make sure the rules are created.
