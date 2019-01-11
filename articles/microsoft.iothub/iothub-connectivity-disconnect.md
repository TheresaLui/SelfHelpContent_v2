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
/>

# Unexpectedly disconnected from IoT Hub

## **Recommended steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId).

1. If you have the error code (400xxx, 500xxx) from diagnostic logs or the device, check if there's solution in our device disconnection guide.<br>
[IoT Hub disconnection errors and solutions](https://aka.ms/iothubdisconnect)

1. If you have access to the device either physically or remotely (like SSH), see if you can get the logs from the device to find out more. These logs will also help our support team to help you troubleshoot.

## **Recommended documents**
[Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)<br>
[Sending Messages to IoT Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)<br>
[Monitoring Device Connections in Real-Time with Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)<br>
[Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)
