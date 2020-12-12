<properties
	pageTitle="Azure Load Balancer configuration issues - Resource Health Status"
	description="Azure Load Balancer configuration issues - Resource Health Status"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781316"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8dab7553-0965-45d3-a66d-895655a50a6k"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer Resource Health Status

## **Recommended Steps**

* Learn more about [how to view resource health status on Azure Portal](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#resource-health-status)
* Learn about specific statuses for the Azure Load Balancer:
  1. *Available*: Your Standard Load Balancer resource is healthy and available
  2. *Degraded*:  Your Standard Load Balancer has platform-initiated or user-initiated events impacting performance. The Datapath Availability metric has reported less than 90% but greater than 25% health for at least two minutes. Follow [these instructions](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-diagnose-my-load-balancer-deployment) to troubleshoot.
  3. *Unavailable*: Your standard Load Balancer is not healthy. The Datapath Availability metric has reported less than 25% health for at least two minutes. Follow [these instructions](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics#how-do-i-diagnose-my-load-balancer-deployment) to troubleshoot.
  4. *Unknown*: Resource health status for your standard load balancer resource has not been updated yet, or has not received Data Path availability information for the last 10 minutes. This state should be transient and will reflect correct status as soon as data is received.
