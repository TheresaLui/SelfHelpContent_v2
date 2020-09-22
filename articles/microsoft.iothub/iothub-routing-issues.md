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
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="8bb9a0cc-e06a-4e76-bca5-3e703c4ab16a"
	ownershipId="AzureIot_IotHub"
/>

# Issues with IoT Hub routing

## **Recommended Steps** 

1. To check the health status of your endpoint, go to **Custom endpoints** in [**Message routing**](data-blade:Microsoft_Azure_IotHub.RoutingBlade.resourceId.$resourceId)
1. To see the traffic, latency, and if messages have been dropped or orphaned, go to [**Metrics**](data-blade:Microsoft_Azure_Monitoring.MetricsBladeV3.ResourceId.$resourceId). For example:

	* Use *Routing: telemetry messages dropped* to see number of messages dropped due to dead endpoints
	* Use *Routing: telemetry messages orphaned* to see number of messages that didn't match any routing rules, including the fallback route
	* Use *Routing: message latency for Event Hub* to see the latency for routing to Event Hub endpoints

1. [Turn on logs for routing](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health) to see if rules evaluate to "undefined", if there are any errors from an endpoint, etc.

**Not receiving any messages?**

Your messages might be getting lost due to the fallback route being disabled. Try **Enable** the fallback route in [**Message routing**](data-blade:Microsoft_Azure_IotHub.RoutingBlade.resourceId.$resourceId).

**Having trouble applying query on the message body?**

If you think IoT Hub isn't evaluating the query expression on message body, make sure contentType is set as application/JSON and contentEncoding is set as UTF-8, UTF-16, or UTF-32 in the [system properties](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-routing-query-syntax#system-properties).

**Body of JSON unreadable when routing to storage?**

When routing to storage with JSON encoding format, you must set the contentType to application/JSON and contentEncoding to UTF-8 in the message system properties. If this is not set, then IoT Hub writes the message in base 64 encoded format.

## **Recommended Documents**

* [Endpoint health status](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints#custom-endpoints)<br>
* [Troubleshooting routing issues](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c#monitoring-and-troubleshooting)<br>
* [IoT Hub routing metrics details](https://docs.microsoft.com/azure/iot-hub/iot-hub-metrics)<br>
* [Learn more about using queries in message routing](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-routing-query-syntax)<br>
* [Learn about routing endpoints](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c#routing-endpoints)