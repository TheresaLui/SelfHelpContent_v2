<properties
	pageTitle="I can't create an IoT hub using ARM Templates, CLI, REST or Service SDK"
	description="I can't create an IoT hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630530,32630537,32630562"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="c011fffa-d2cf-47bb-b2df-1e2850fb7044"
	ownershipId="AzureIot_IotHub"
/>

# Unable to create an IoT hub using ARM Templates, CLI, REST or Service SDK

## **Recommended Steps**

1. If you got an [error](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors) similar to NoRegisteredProviderFound or MissingSubscriptionRegistration, the issue might be due to the IoT Hub resource provider (Microsoft.Devices) not being registered to your subscription. [Register the **Microsoft.Devices** resource provider](data-blade:HubsExtension.RPStatusBlade.subscriptionId.$subscriptionId) then try again. 
1. If it is already registered and still you cannot create an Iot hub, see if you can create it via Azure Portal
1. If you still can not create an IoT Hub, please wait 15 minutes and try again
