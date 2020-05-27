<properties
	pageTitle="How do I keep track of device connection state reliably and quickly?"
	description="How do I keep track of device connection state reliably and quickly?"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-development-conectivity-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# How do I keep track of device connection state reliably and quickly?

## **Recommended Steps**

* To quickly and reliably keep track of device connection state, we recommend subscribing to the device connection events on Event Grid:

	* [Order device connection events from Azure IoT Hub using Azure Cosmos DB](https://docs.azure.cn/iot-hub/iot-hub-how-to-order-connection-state-events)

**Note**: The `connectionState` field in IoT Hub identity registry is only for debugging and development purposes: [Understanding the IoT Hub device registry](https://docs.azure.cn/iot-hub/iot-hub-devguide-identity-registry#device-heartbeat)
