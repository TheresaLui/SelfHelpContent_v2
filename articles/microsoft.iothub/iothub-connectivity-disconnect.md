<properties
	pageTitle="Unexpectedly disconnected from IoT Hub"
	description="Unexpectedly disconnected from IoT Hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="generic"
	supportTopicIds="32630568"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="18d13f56-abed-4610-a8ce-0d9dd58d78a9"
	ownershipId="AzureIot_IotHub"
/>

# Unexpectedly disconnected from IoT Hub

## **Recommended Steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)

1. For the most reliable connectivity, try using the latest version of our [device client SDKs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks#azure-iot-hub-device-sdks) if possible.

1. Get the error code(s) (400xxx, 500xxx) from diagnostic logs and check if there's solution in our device disconnection guide: [IoT Hub disconnection errors and solutions](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity).

1. If you have access to the device either physically or remotely (like SSH), see if you can get the logs from the device to find out more. These logs will also help our support team to help you troubleshoot.

## **Recommended Documents**

* [Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)<br>
* [Sending Messages to IoT Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)<br>
* [Monitoring Device Connections in Real-Time with Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)<br>
* [Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)
