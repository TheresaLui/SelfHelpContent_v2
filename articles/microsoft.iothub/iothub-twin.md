<properties
	pageTitle="Issues with twin reads or updates"
	description="Issues with twin reads or updates"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="generic"
	supportTopicIds="32630546"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="f4c81c07-9b2e-4769-a187-2098d8d5cbb9"
	ownershipId="AzureIot_IotHub"
/>

# Issues with twin reads or updates

## **Recommended Steps**

1. Ensure device is registered. See [404001 DeviceNotFound](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404001-devicenotfound).
1. Ensure that there's no more than one connection per client. See [400027 ConnectionForcefullyClosedOnNewConnection](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-400027-connectionforcefullyclosedonnewconnection)
1. Your device might have connection problems. See [404104 DeviceConnectionClosedRemotely](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404104-deviceconnectionclosedremotely).

## **Recommended Documents**

* [Understand device twins](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins)<br>
* [Understand module twins](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins)<br>
* [Common error codes](https://docs.microsoft.com/rest/api/iothub/common-error-codes)<br>

