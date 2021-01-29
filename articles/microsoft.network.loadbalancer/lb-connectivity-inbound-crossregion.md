<properties
	pageTitle="Azure Load Balancer Connectivity Issues - Cannot connet to a Cross-region Load Balancer"
	description="Azure Load Balancer Connectivity Issues - Cannot connect to a Cross-region Load Balancer"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32750779"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7554-0965-45d3-a66d-895655a50a6g"
	ownershipId="CloudNet_LoadBalancer"
/>

# No inbound connectivity to frontend IP of Azure Load Balancer

## **Recommended Steps**

* Use the [data path availability metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#is-the-data-path-up-and-available-for-my-load-balancer-frontend) to confirm that the data path of the Cross-region Load Balancer is down, and therefore allowing no inbound connectivity.
* Use the [data path availability metric](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#is-the-data-path-up-and-available-for-my-load-balancer-frontend) to confirm that the data path of the Regional Load Balancers in the backend pool of Cross-region Load Balancer is down. If all the regional Load Balancers have data path availablity of less than 100%, follow the [troubleshooting guide](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-diagnose-my-load-balancer-deployment) to bring the regional Load Balancers up.  
* A [load balancing rule](https://docs.microsoft.com/azure/load-balancer/quickstart-load-balancer-standard-public-portal?tabs=option-1-create-load-balancer-standard#create-a-load-balancer-rule) is required to establish an inbound connection. Make sure the rules are created.
* Make sure the frontend and backend ports of the Cross-region Load Balancer load balancing rule matches the frontend port of the Regional Load Balancer load balancing rule. 
