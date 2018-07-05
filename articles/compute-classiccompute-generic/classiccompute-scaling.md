<properties
	pageTitle="worker role (paas)/configuration and management/scaling"
	description="worker role (paas)/configuration and management/scaling"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="ChiragPavecha"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32569897"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public"
/>

# worker role (paas)/configuration and management/scaling

## **Recommended steps**
Recommended steps to try:<br>

* Ensure that all roles instances are in Ready state. Autoscaling only occurs if all roles are in Ready state.<br>

* Try to scale manually.<br>
  If manual scaling succeeds, it may indicate that the autoscale profile is configured incorrectly. Multiple autoscale profiles can affect the behavior of autoscale. It is recommended to create and manage autoscale profiles from the [new portal](https://portal.azure.com).<br>
	
* Try scaling in smaller increments.<br> It may be successful if the cluster where your Cloud Service is deployed is low on resources. When scaling existing Cloud Services, the compute resources can be allocated only from the cluster where your service is deployed. For more information, see    [Troubleshooting allocation failure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures).<br>

* Increase the subscription quota limit by contacting Microsoft, because autoscaling cannot succeed without sufficient compute quota.<br>

* Create a host service and redeploy to it with the maximum instances required and scale down to a smaller number of instances if needed. Deploying with maximum instances ensures the cluster has the capacity you may require.<br>

For more information, see [Autoscaling best practices](https://docs.microsoft.com/azure/best-practices-auto-scaling).

## **Recommended documents**
[How to Scale your Cloud Services?](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-scale/) <br>
[Not able to scale more than 25 instances?](https://azure.microsoft.com/documentation/articles/vs-azure-tools-debug-cloud-services-virtual-machines/#limitations-of-remote-debugging-in-azure)<br>
[Auto-Scaling isn't happening as expected?](https://blogs.msdn.microsoft.com/cie/2017/01/03/troubleshooting-azure-auto-scale-profile-does-not-change/)<br>
[Auto-Scale Notifications about "Metrics data not available"](https://social.msdn.microsoft.com/Forums/bc2048c4-8d49-4c54-b150-f263808c4b7a/notification-could-not-automatically-scale-xxx-because-monitoring-data-was-not-found?forum=windowsazuremanagement)

