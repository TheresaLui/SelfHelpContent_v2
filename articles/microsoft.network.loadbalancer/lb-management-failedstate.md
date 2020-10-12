<properties
	pageTitle="Azure Load Balancer Management Issues - Resource In Failed State"
	description="Azure Load Balancer Management Issues - Resource In Failed State"
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
	articleId="8deb7553-0965-45d3-a66d-895655a50a6d"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer In Failed State issues

## **Recommended Stesps**
1. Go to [https://resources.azure.com](https://resources.azure.com), and sign in with your Azure portal credentials. 
2. Select Read/Write. 
3. On the left, expand Subscriptions, and then expand the Subscription with the Load Balancer to update. 
4. Expand ResourceGroups, and then expand the resource group with the Load Balancer to update. 
5. Select Microsoft.Network > LoadBalancers, and then select the Load Balancer to update, LoadBalancer_1. 
6. On the display page for LoadBalancer_1, select GET > Edit. 
7. Update the ProvisioningState value from Failed to Succeeded. 
8. Select PUT. 
