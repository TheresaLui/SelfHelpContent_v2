<properties
	pageTitle="I don't understand why I'm getting this error"
	description="I don't understand why I'm getting this error"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32596605,32596633,32596647"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# I don't understand why I'm getting this error

## **Recommended steps**

1. Turn on debug mode on the device ([C#](https://github.com/Azure/azure-iot-sdk-csharp/tree/master/tools/CaptureLogs), [Node](https://github.com/Azure/azure-iot-sdk-node/wiki/Troubleshooting-Guide-Devices#cannot-connect-to-your-azure-iot-hub)) and retry. The logs might give more you better idea of what the error is.

1. [Turn on](data-blade:Microsoft_Azure_Monitoring.DiagnosticsLogsBlade.id.$resourceId) and go through [IoT Hub diagnostics logs](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health). These logs might give you more information on if there was a server side error. Check our docs on explanation and solution for common errors.<br>
[IoT Hub REST API error codes](https://docs.microsoft.com/rest/api/iothub/common-error-codes)<br>
[IoT Hub disconnection errors and solutions](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity)

## **Recommended documents**
[Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)