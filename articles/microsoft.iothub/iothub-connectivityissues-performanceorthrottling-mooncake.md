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
/>

# Issues with device-to-cloud messages

## **Recommended Steps**

1. If all of your messages are timing out, make sure that you haven't run out of your daily message quota by checking the overview page: [IoT Hub quotas and pricing](https://www.azure.cn/pricing/details/iot-hub/)
2. Check if you're hitting the throttle limit by comparing your [traffic](data-blade:Microsoft_Azure_Monitoring.MetricsBladeV3.ResourceId.$resourceId) against our [documentation](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling)
3. If you're running tests and wondering why IoT Hub isn't returning any 429 errors for throttling, it's because IoT Hub only returns 429 ThrottlingException after the limit is violated for too long. We do this so that your messages aren't dropped if you get burst traffic. In the meantime, IoT Hub processes the messages at the operation throttle rate, which might be slow if there's too much traffic in the backlog: [IoT Hub quotas and throttling](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling)
4. Try running the [diagnostic tool](https://github.com/Azure/iothub-diagnostics) to check connectivity issues

## **Recommended Documents**

* [Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)
* [Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.azure.cn/iot-hub/iot-hub-monitor-resource-health)
* [Scale your IoT hub solution](https://docs.azure.cn/iot-hub/iot-hub-scaling)
