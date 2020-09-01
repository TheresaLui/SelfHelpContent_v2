<properties
	pageTitle="I'm hitting quota limits for my IoT hub"
	description="I'm hitting quota limits for my IoT hub"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680950,32680966,32680969,32680976,32680986"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="06c4e95e-448b-4ac6-9ebc-57c7c2fd38e3"
	ownershipId="AzureIot_IotEdge"
/>

# I'm hitting quota limits for my IoT hub

If you reach the IoT Hub message quota (403 IoTHubQuotaExceeded), consider upgrading your IoT Hub to a higher tier to suit the needs of your solution.

## **Recommended Steps**

* To upgrade IoT hub to a higher tier, go to [Pricing and scale](data-blade:Microsoft_Azure_IotHub.IotHubPricingAndScaleBlade.id.$resourceId), and [choose a tier](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
* It is not currently possible to upgrade from IoT Hub free edition (F1) to one of the paid editions. For a workaround, use [ARM templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-export-template-powershell) to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our [bulk device management API](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt).
* You can ask for other types of quota increases, like maximum units, number of hubs in a subscription, or maximum device count, in a support request

## **Recommended Documents**

* [Azure IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)
* [Understand IoT Hub quotas](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)
* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade)
* [Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
