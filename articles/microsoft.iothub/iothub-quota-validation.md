<properties
	pageTitle="Quota validation issues"
	description="Quota validation issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596659"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Quota validation issues

## **Recommended steps**

1. If you think that you hit the message quota way quicker than expected (403 IotHubQuotaExceeded), it might be because you're on the free (F1) edition, which has a smaller chunking limit at 0.5KB (as opposed to 4KB for the paid editions). <br>
[Understand IoT Hub quotas](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)

1. [Unfortunately, it's not possible to upgrade from free IoT Hub to paid](https://azure.microsoft.com/pricing/details/iot-hub/). For a workaround, use ARM templates to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our bulk device management API.<br>
[Export a resource group as ARM template](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-export-template-powershell)<br>
[IoT Hub bulk device management](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt)

## **Recommended documents**
[How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade) <br>
[IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)<br>
[Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
