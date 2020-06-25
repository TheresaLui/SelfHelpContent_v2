<properties
	pageTitle="How do I keep track of device connection state reliably and quickly?"
	description="How do I keep track of device connection state reliably and quickly?"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="99"
	selfHelpType="resource"
	supportTopicIds="32630544"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"
	articleId="9d5822b4-1775-42a1-af9e-a691bb6ade57"
	ownershipId="AzureIot_IotHub"
/>

# How do I keep track of device connection state reliably and quickly?

## **Recommended Steps**

1. To quickly and reliably keep track of device connection state, we recommend subscribing to the device connection events on Event Grid:

	* [IoT Hub and Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid#event-types)<br>
	* [Order device connection events from Azure IoT Hub using Azure Cosmos DB](https://docs.microsoft.com/azure/iot-hub/iot-hub-how-to-order-connection-state-events)

**Note**: The `connectionState` field in IoT Hub identity registry is only for debugging and development purposes: [Understanding the IoT Hub device registry](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-identity-registry#device-heartbeat)
