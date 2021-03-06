<properties
	pageTitle="Issues with device-to-cloud messages"
	description="Issues with device-to-cloud messages"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-connectivityissues-performanceorthrottling-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# Issues with device-to-cloud messages

## **Recommended Steps**

1. If all of your messages are timing out, go to [**Overview**](data-blade:Microsoft_Azure_IotHub.IotHubOverviewBlade.id.$resourceId) and make sure you're still under your daily limit
2. Check if you're hitting the throttle limit by comparing your [*telemetry message send attempts* metric](data-blade:Microsoft_Azure_Monitoring.MetricsBladeV3.ResourceId.$resourceId) against our [documentation](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling)
3. Consider [scaling up your IoT Hub](https://docs.azure.cn/iot-hub/iot-hub-scaling) if you're running into quota or throttling limits
4. If you have access to the device, try running the [diagnostic tool](https://github.com/Azure/iothub-diagnostics) on it to check connectivity issues

**Where are my 429 errors?**

If you're running tests and wondering why IoT Hub isn't returning any 429 errors for throttling, it's because IoT Hub only returns 429 ThrottlingException after the limit is violated for too long. We do this so that your messages aren't dropped if you get burst traffic. In the meantime, IoT Hub processes the messages at the operation throttle rate, which might be slow if there's too much traffic in the backlog. To learn more, see [IoT Hub traffic shaping](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling#traffic-shaping).

## **Recommended Documents**

* [Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)
* [Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.azure.cn/iot-hub/iot-hub-monitor-resource-health)
* [Scale your IoT hub solution](https://docs.azure.cn/iot-hub/iot-hub-scaling)
