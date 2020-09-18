<properties
	pageTitle="How to get more details on IoT Hub errors"
	description="How to get more details on IoT Hub errors"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-errorsandexceptionsissues-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# How to get more details on IoT Hub errors

## **Recommended Steps**

1. Turn on debug mode on the device ([C#](https://github.com/Azure/azure-iot-sdk-csharp/tree/master/tools/CaptureLogs), [Node](https://github.com/Azure/azure-iot-sdk-node/wiki/Troubleshooting-Guide-Devices#cannot-connect-to-your-azure-iot-hub)) and retry. The logs might give more you better idea of what the error is.
2. [Turn on](data-blade:Microsoft_Azure_Monitoring.DiagnosticsLogsBlade.id.$resourceId) and go through [IoT Hub diagnostics logs](https://docs.azure.cn/iot-hub/iot-hub-monitor-resource-health). These logs might give you more information on if there was a server side error. Check the recommended documents for explanations and solutions for common errors.

## **Recommended Documents**

* [IoT Hub REST API error codes](https://docs.microsoft.com/rest/api/iothub/common-error-codes)
* [IoT Hub disconnection errors and solutions](https://docs.azure.cn/iot-hub/iot-hub-troubleshoot-connectivity)
* [Benefits of using the Azure IoT SDKs](https://azure.microsoft.com/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)
