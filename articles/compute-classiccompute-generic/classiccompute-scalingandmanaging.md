<properties
	pageTitle="worker role (paas)/configuration and management/scaling and managing"
	description="worker role (paas)/configuration and management/scaling and managing"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="ChiragPavecha"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553317"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public"
/>

# worker role (paas)/application and service availability/scaling and managing

## **Recommended steps**
Azure Autoscale requires monitoring data from the role instances to scale. At times, there may be a delay in data collection.
When Autoscale [cannot get the metrics data](https://social.msdn.microsoft.com/Forums/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement) it scales to the default instance count if that value is higher than the current instance count.
This issue corrects itself when Autoscale starts to receive the metrics data again. The recommended value for TimeWindow is 30 minutes or greater.
For more information, see [Autoscaling best practices](https://docs.microsoft.com/azure/best-practices-auto-scaling).

Additional steps to try:<br>

•	Ensure that all roles instances are in Ready state. Autoscaling only occurs if all roles are in Ready state.<br>

•	Try to scale manually.<br>
	If manual scaling succeeds, it may indicate that the autoscale profile is configured incorrectly. Multiple autoscale profiles can affect the behavior of autoscale. It is recommended to create and manage autoscale profiles from the [new portal](https://portal.azure.com).<br>
	
•	Try scaling in smaller increments.<br> It may be successful if the cluster where your Cloud Service is deployed is low on resources. When scaling existing Cloud Services, the compute resources can be allocated only from the cluster where your service is deployed. For more information, see [Troubleshooting allocation failure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures).<br>

•	Increase the subscription quota limit by contacting Microsoft, because autoscaling cannot succeed without sufficient compute quota.<br>

•	Create a host service and redeploy to it with the maximum instances required and scale down to a smaller number of instances if needed. Deploying with maximum instances ensures the cluster has the capacity you may require.<br>


## **Recommended documents**
[How to Scale your Cloud Services?](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-scale/) <br>
[Not able to scale more than 25 instances?](https://azure.microsoft.com/documentation/articles/vs-azure-tools-debug-cloud-services-virtual-machines/#limitations-of-remote-debugging-in-azure)<br>
[Auto-Scale Notifications about "Metrics data not available"](https://social.msdn.microsoft.com/Forums/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement)<br>

[How to manage (swap/delete deployment, link to a resource) Cloud Services?](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-manage/) <br>
[How to move the Cloud Services between Resource Groups and what are the limitations?](https://azure.microsoft.com/documentation/articles/resource-group-move-resources/#classic-deployment-limitations)
[How to configure the VM size for Cloud Services Role](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs#configure-sizes-for-cloud-services)<br>
[How to change the VM size of an exiting Cloud Services Role](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs#changing-the-size-of-an-existing-role)
