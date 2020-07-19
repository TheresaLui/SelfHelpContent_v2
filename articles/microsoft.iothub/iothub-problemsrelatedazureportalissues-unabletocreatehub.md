<properties
	pageTitle="I can't create an IoT hub"
	description="I can't create an IoT hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630529"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="57df07ed-044a-443b-9f35-7dd0ac591c62"
	ownershipId="AzureIot_IotHub"
/>

# Unable to create an IoT hub

## **Recommended Steps**

1. If you receive an error similar to NoRegisteredProviderFound or MissingSubscriptionRegistration, the issue might be due to the IoT Hub resource provider (Microsoft.Devices) not being [registered to your subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors). [Register the **Microsoft.Devices** resource provider](data-blade:HubsExtension.RPStatusBlade.subscriptionId.$subscriptionId) then try again.
1. If it is already registered and still you cannot create an Iot hub, see if you can create it via Azure [CLI](https://docs.microsoft.com/azure/iot-hub/iot-hub-create-using-cli) or [PowerShell](https://docs.microsoft.com/azure/iot-hub/iot-hub-create-using-powershell)
1. If you still can not create an IoT Hub, please wait 15 minutes and try again.
