<properties
	pageTitle="When using Autoscale, I get an email stating 'metrics data not available'"
	description="When using Autoscale, I get an email stating 'metrics data not available'"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public, fairfax, MoonCake, usnat, ussec"
	articleId="7f1012c9-9029-41ba-b879-6344a8fbd317"
	ownershipId="Compute_VirtualMachines"
/>

# When using Autoscale, I get an email stating 'metrics data not available'

Autoscale requires monitoring data from the role instances to scale. At times, there may be a delay in data collection. When autoscale cannot get the metrics data, it scales to the **Default Value** if it is higher than the current instance count. This issue corrects itself when autoscale starts receiving the metrics data. <br>

## **Recommended steps**

1. If you are having issues in production, turn off autoscale and manually scale to the number of instances needed.<br>
2. Set your scaling **TimeWindow** (duration) to 30 minutes or higher.

## **Recommended documents**

* [About lack of monitoring data](https://social.msdn.microsoft.com/Forums/azure/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement).
