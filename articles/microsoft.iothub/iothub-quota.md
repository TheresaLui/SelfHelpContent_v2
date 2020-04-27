<properties
	pageTitle="Manage your IoT Hub pricing or scale"
	description="Manage your IoT Hub pricing or scale"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32630557,32630561"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="6a85270e-9f76-4a77-bdba-79c38d4a5461"
	ownershipId="AzureIot_IotHub"
/>

# Manage your IoT Hub pricing or scale

## **Recommended Steps**

1. To upgrade IoT hub to a higher tier, go to [**Pricing and scale**](data-blade:Microsoft_Azure_IotHub.IotHubPricingAndScaleBlade.id.$resourceId), and [choose a tier](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
1. It is [not currently possible](https://azure.microsoft.com/pricing/details/iot-hub/) to upgrade from IoT Hub free edition (F1) to one of the paid editions. For a workaround, use [ARM templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-export-template-powershell) to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our [bulk device management API](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt).
1. For other types of quota increases, like maximum units, number of hubs in a subscription, or maximum device count, please open a support request

## **Recommended Documents**

* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade)<br>
* [IoT hub pricing examples](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-pricing)<br>
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)<br>
