<properties
	pageTitle="Quota validation issues"
	description="Quota validation issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596659,32630567"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="07984f0e-a641-4843-a804-e8015906371d"
/>

# Quota validation issues

## **Recommended Steps**

1. If you think that you hit the message quota sooner than expected (403 IotHubQuotaExceeded), it might be because you're on the free (F1) edition, which has a smaller chunking limit at 0.5KB (as opposed to 4KB for the paid editions): [Understand IoT Hub quotas](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)
1. [Unfortunately, it's not possible to upgrade from free IoT Hub to paid](https://azure.microsoft.com/pricing/details/iot-hub/). For a workaround, use [ARM templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-export-template-powershell) to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our [bulk device management API](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt).<br>

## **Recommended Documents**

* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade) <br>
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)<br>
* [Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
