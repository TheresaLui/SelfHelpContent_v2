<properties
  pagetitle="Unexpectedly disconnected from IoT Hub"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,yiygu,jtanner"
  selfhelptype="Generic"
  supporttopicids="32630568"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="18d13f56-abed-4610-a8ce-0d9dd58d78a9"
  ownershipid="AzureIot_IotHub" />
# Unexpectedly disconnected from IoT Hub

## **Recommended Steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
1. For the most reliable connectivity, try using the latest version of our [device client SDKs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks#azure-iot-hub-device-sdks) if possible
1. Get the error code(s) (400xxx, 500xxx) from diagnostic logs and refer to the corresponding device disconnection troubleshooting guide: 

   * [404104 DeviceConnectionClosedRemotely](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404104-deviceconnectionclosedremotely)
   * [401003 IoTHubUnauthorized](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-401003-iothubunauthorized)
   * [409002 LinkCreationConflict](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-409002-linkcreationconflict)
   * [500xxx Internal errors](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-500xxx-internal-errors)
   * [500008 GenericTimeout](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-500xxx-internal-errors)
   
1. If you have access to the device either physically or remotely (like SSH), see if you can get the logs from the device to find out more. These logs will also help our support team to help you troubleshoot.

1. To quickly and reliably keep track of device connection state, we recommend subscribing to the device connection events on Event Grid: 

 

   * [IoT Hub and Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid#event-types)

   * [Order device connection events from Azure IoT Hub using Azure Cosmos DB](https://docs.microsoft.com/azure/iot-hub/iot-hub-how-to-order-connection-state-events) 

 

**Note**: The `connectionState` field in IoT Hub identity registry is only for debugging and development purposes: [Understanding the IoT Hub device registry](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-identity-registry#device-heartbeat) 

## **Recommended Documents**

* [Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)
* [Sending Messages to IoT Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)
* [Monitoring Device Connections in Real-Time with Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)
* [Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)