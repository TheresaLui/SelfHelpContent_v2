<properties 
	pageTitle="When using Autoscale, I get error 'Metrics data not available'"
	description="When using Autoscale, I get error 'Metrics data not available'"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public"
/>

# When using Autoscale, I get error 'Metrics data not available'
Autoscale requires monitoring data from the role instances in order to scale. At times there may be a delay in data collection. When autoscale cannot get the metrics data, it will scale to the **Default Value** if it is higher than the current instance count. This issue will correct itself when autoscale starts receiving the metrics data. <br>
## **Recommended steps**
1. If this is causing production issues, turn off autoscale and manually scale to the number of instances needed.
2. Set your scaling **TimeWindow** (duration) to 30 minutes or higher.

## **Recommended documents**
[About lack of monitoring data] (https://social.msdn.microsoft.com/Forums/azure/en-US/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement) <br>