<properties
	pageTitle="Issues connecting a device to IoT Hub for the first time"
	description="Issues connecting a device to IoT Hub for the first time"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	authorAlias="jlian"
	selfHelpType="generic"
	supportTopicIds="32630541"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Issues connecting a device to IoT Hub for the first time

## **Recommended steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId).

1. Try testing the connection with a default sample and running our diagnostic tool. <br>
[Tutorial: use a simulated device to test connectivity](https://docs.microsoft.com/azure/iot-hub/tutorial-connectivity)<br>
[IoT Hub connection diagnostic tool](https://github.com/azure/iothub-diagnostics)

1. If you can get the sample to work, but not your own application, check to see if there's an authorization or firewall issue. <br>
[IoT Hub device side troubleshooting guide](https://github.com/Azure/azure-iot-sdk-node/wiki/Troubleshooting-Guide-Devices#cannot-connect-to-your-azure-iot-hub)

1. If you have access to the device either physically or remotely (like SSH), see if you can get the logs from the device to find out more. These logs will also help our support team to help you troubleshoot.


## **Recommended documents**
[Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)<br>
[Sending Messages to IoT Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)<br>
[Monitoring Device Connections in Real-Time with Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)<br>
[Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)