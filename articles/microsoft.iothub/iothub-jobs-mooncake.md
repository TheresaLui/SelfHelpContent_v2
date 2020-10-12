<properties
	pageTitle="IoT Hub job issues"
	description="IoT Hub job issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="12"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-jobs-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub job issues

## **Recommended Steps**

* There are limitations on the [number of concurrent jobs](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) that can be run based on the SKU of IoT Hub
* There are also throttles on the [number of job operations and job device operations](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that can happen per second
* You can only have one active device import/export job at a time

## **Recommended Documents**

* [IoT Hub quotas and throttling](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling)
* [Schedule jobs on multiple devices](https://docs.azure.cn/iot-hub/iot-hub-devguide-jobs)
* [Manage your IoT Hub device identities in bulk](https://docs.azure.cn/iot-hub/iot-hub-bulk-identity-mgmt)
