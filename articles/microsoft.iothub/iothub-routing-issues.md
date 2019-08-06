<properties
	pageTitle="Issues with IoT Hub routing"
	description="Issues with IoT Hub routing"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="generic"
	supportTopicIds="32680885,32680884"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="8bb9a0cc-e06a-4e76-bca5-3e703c4ab16a"
/>

# Issues with IoT Hub routing

## **Recommended Steps** 

1. To check the health status of your endpoint, go to **Custom endpoints** in [**Message routing**](data-blade:Microsoft_Azure_IotHub.RoutingBlade.id.$resourceId)
1. To see the traffic, latency, and if messages have been dropped or orphaned, go to [**Metrics**](data-blade:Microsoft_Azure_Monitoring.MetricsBladeV3.ResourceId.$resourceId). For example:

	* Use *Routing: telemetry messages dropped* to see number of messages dropped due to dead endpoints
	* Use *Routing: telemetry messages orphaned* to see number of messages that didn't match any routing rules, including the fallback route
	* Use *Routing: message latency for Event Hub* to see the latency for routing to Event Hub endpoints

1. [Turn on logs for routing](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health) to see if rules evaluate to "undefined", if there are any errors from an endpoint, etc.

## **Recommended Documents**

* [Endpoint health status](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints#custom-endpoints)<br>
* [Troubleshooting routing issues](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c#monitoring-and-troubleshooting)<br>
* [IoT Hub routing metrics details](https://docs.microsoft.com/azure/iot-hub/iot-hub-metrics)

