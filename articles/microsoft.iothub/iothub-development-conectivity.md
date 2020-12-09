<properties
  pagetitle="How do I keep track of device connection state reliably and quickly?&#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner,yiygu"
  selfhelptype="Resource"
  supporttopicids="32630541,32630540,32783516,32630568"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,usnat,ussec,mooncake"
  articleid="9d5822b4-1775-42a1-af9e-a691bb6ade57"
  ownershipid="AzureIot_IotHub" />
# How do I keep track of device connection state reliably and quickly?

## **Recommended Steps**

1. To quickly and reliably keep track of device connection state, we recommend subscribing to the device connection events on Event Grid:

	* [IoT Hub and Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid#event-types)
	* [Order device connection events from Azure IoT Hub using Azure Cosmos DB](https://docs.microsoft.com/azure/iot-hub/iot-hub-how-to-order-connection-state-events)

**Note**: The `connectionState` field in IoT Hub identity registry is only for debugging and development purposes: [Understanding the IoT Hub device registry](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-identity-registry#device-heartbeat)