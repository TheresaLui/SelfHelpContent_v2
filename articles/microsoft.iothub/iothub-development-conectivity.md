<properties
	pageTitle="How do I keep track of device connection state reliably and quickly?"
	description="How do I keep track of device connection state reliably and quickly?"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32596623,32596629"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# How do I keep track of device connection state reliably and quickly?

## **Recommended documents**

1. To quickly and reliably keep track of device connection state, we recommend subscribing to the device connection events on Event Grid. <br>
[IoT Hub and Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid#event-types)<br>
[Order device connection events from Azure IoT Hub using Azure Cosmos DB](https://docs.microsoft.com/azure/iot-hub/iot-hub-how-to-order-connection-state-events)

2. The `connectionState` field in IoT Hub identity registry is only for debugging and development purposes. <br>
[Understanging the IoT Hub device registry](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-identity-registry#device-heartbeat)
