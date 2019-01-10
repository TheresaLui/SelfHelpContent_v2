<properties
	pageTitle="I'm seeing performance or throttling issues"
	description="I'm seeing performance or throttling issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32596652,32596653,32596667"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# I'm seeing performance or throttling issues

## **Recommended steps**

1. If all of your messages are timing out, make sure that you haven't run out of quota by checking the overview page. <br>
[IoT Hub quotas and pricing](https://azure.microsoft.com/pricing/details/iot-hub/)

1. Also check if you're hitting the throttle limit by comparing your [traffic](data-blade:Microsoft_Azure_Monitoring.MetricsBladeV3.ResourceId.$resourceId) against our [documentation](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling).

1. If you're running tests and wondering why IoT Hub isn't returning any 429 errors for throttling, it's because IoT Hub only returns 429 ThrottlingException after the limit is violated for too long. We do this so that your messages aren't dropped if you get burst traffic. In the meantime, IoT Hub processes the messages at the operation throttle rate, which might be slow if there's too much traffic in the backlog. <br> 
[IoT Hub quotas and throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)

## **Recommended documents**
[Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)<br>
[Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)<br>
[Scale your IoT hub solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)<br>