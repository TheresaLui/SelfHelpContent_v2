<properties 
	pageTitle="My autoscale is not working"
	description="My autoscale is not working"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public"
/>

# My autoscale is not working

## **Recommended steps**
Instances are not scaling based on CPU or other default metrics, for example: **CPU** > 80% and have the **TimeWindow** set as 45 minutes.

In this example, scaling will happen only when the average CPU value for *all* role instances is more than 80% for at least 45 minutes.

1. Reduce the **TimeWindow** property. <br>
This will cause scaling to happen more frequently. The default **TimeWindow/Duration** property is 30 minutes  (new portal) or 45 minutes (classic portal).

## **Recommended documents**
[About autoscale best practices](https://azure.microsoft.com/documentation/articles/insights-autoscale-best-practices/) <br>
[About scaling Cloud Services in Portal](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-scale-portal/)