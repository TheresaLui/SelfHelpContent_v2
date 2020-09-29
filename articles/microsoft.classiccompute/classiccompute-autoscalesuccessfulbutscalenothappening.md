<properties
	pageTitle="Autoscale seems to be successful but scaling is not happening"
	description="Autoscale seems to be successful but scaling is not happening"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ccc6b548-ea22-4b67-b9fa-6198ad4badad"
	ownershipId="Compute_VirtualMachines"
/>

# Autoscale seems to be successful but scaling is not happening

The following is a collection of solutions and explanations for why scaling may not occur.<br>

## **Recommended steps**

1. Ensure that all roles instances are in **Ready** state. Autoscale only happens if all roles are in Ready state.<br>

	Try to scale manually. If a manual scale succeeds, it may indicate that the autoscale profile is configured incorrectly. Multiple autoscale profiles can affect the behavior of autoscale. [Creating and managing autoscale profiles](https://azure.microsoft.com/documentation/articles/insights-autoscale-best-practices/#autoscale-concepts) should be done from the same portal as each portal has unique default autoscale profiles.<br>

2. Try to scale in smaller increments as the cluster where your application is deployed may not have enough free cores.<br>

	Increase the subscription quota limit by [contacting Microsoft](data-blade:Microsoft_Azure_Support.NewSupportRequestBlade.assetId.$resourceId) as autoscale cannot succeed without sufficient compute quota.<br>

3. Create a host service and redeploy to it with the maximum instances needed. Scale down afterwards if needed.

	Deploying with maximum instances ensures the cluster has the capacity you may require.<br>

## **Recommended documents**

* [About autoscale best practices](https://azure.microsoft.com/documentation/articles/insights-autoscale-best-practices/#autoscale-best-practices)<br>
* [About Cloud Services allocation failures](https://azure.microsoft.com/documentation/articles/cloud-services-allocation-failures/)
