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
	cloudEnvironments="public"
/>

# Autoscale seems to be successful but scaling is not happening

## **Recommended steps**
1. Ensure that all roles instances are in **Ready** state. <br>
2. Try to scale manually. <br>
3. Check the number of available cores. <br>
If your subscription has reached the maximum compute cores, you can increase the subscription compute quota limit by [contacting Microsoft] (data-blade:Microsoft_Azure_Support.NewSupportRequestBlade).
4. This may happen when the cluster you are deployed to has reached capacity limits or does not have the type of compute cores that you are requesting. <br>
    * Try to scale in smaller increments. <br>
    * Create a new host service and redeploy to it with the maximum instances needed. Scale down after the initial deployment if needed. Deploying with maximum instances ensures that the cluster has the capacity you may need. <br>

## **Recommended documents**
[About Cloud Services allocation failures] (https://azure.microsoft.com/documentation/articles/cloud-services-allocation-failures/) <br>
