<properties
	pageTitle="I'm seeing connectivity issues with my IoT devices"
	description="I'm seeing connectivity issues with my IoT devices"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32596603,32596668,32596620,32596621,32596622"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="88730035-f99d-44e6-900f-fdaa9d066f27"
/>

# I'm seeing connectivity issues with my IoT devices

## **Recommended Steps**

1. Make sure the device isn't accidentally disabled in [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
2. If you're having trouble connecting your device to IoT Hub for the first time, try testing the connection with a [default sample](https://docs.microsoft.com/azure/iot-hub/tutorial-connectivity) and running our [diagnostic tool](https://github.com/azure/iothub-diagnostics)
3. If you can get the sample to work but not your own application, check to see if there's an authorization or firewall issue: [IoT Hub device side troubleshooting guide](https://github.com/Azure/azure-iot-sdk-node/wiki/Troubleshooting-Guide-Devices#cannot-connect-to-your-azure-iot-hub)
4. If the device was connected to IoT Hub but the connection dropped unexpectedly, get the error code(s) (400xxx, 500xxx) from diagnostic logs and check if there's solution in our device disconnection guide: [IoT Hub disconnection errors and solutions](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity)
5. If you have access to the device either physically or remotely (like SSH), see if you can get the logs from the device to find out more. These logs will also help our support team to help you troubleshoot.

## **Recommended Documents**

* [Diagnosing IoT Hub Issues](https://github.com/Azure/iothub-diagnostics)<br>
* [Sending Messages to IoT Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c)<br>
* [Monitoring Device Connections in Real-Time with Event Grid](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid)<br>
* [Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)
