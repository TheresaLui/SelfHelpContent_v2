<properties
	pageTitle="Azure Load Balancer Management Issues - Cannot delete load balancer"
	description="Azure Load Balancer Management Issues - Cannot delete load balancer"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781322"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6d"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer delete issues

## **Recommended Steps**

If your load balancer is in a failed state, follow these steps to bring it back from the failed state:

1. Go to [Azure Resource Explorer)[https://resources.azure.com] and sign in with your Azure Portal credentials.
2. Select **Read/Write**.
3. On the left, expand **Subscriptions**, and then expand the Subscription with the Load Balancer to update.
4. Expand **ResourceGroups**, and then expand the resource group with the Load Balancer to update.
5. Select **Microsoft.Network** > **LoadBalancers**, and then select the Load Balancer to update, LoadBalancer_1.
6. On the display page for LoadBalancer_1, select **GET** > **Edit**.
7. Update the `ProvisioningState` value from `Failed` to `Succeeded`.
8. Select **PUT**.
* If the load balancer has virtual machine scale sets in the backend pool, follow the [instructions](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-virtual-machine-scale-sets#inbound-nat-pool) on how to delete inbound NAT pool first.
