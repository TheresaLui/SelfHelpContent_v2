<properties
	pageTitle="I can't create an IoT hub using ARM Templates, CLI, REST or Service SDK"
	description="I can't create an IoT hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630530,32630537,32630562"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Unable to create an IoT hub using ARM Templates, CLI, REST or Service SDK

## **Recommended steps**

1. If you got an error similar to NoRegisteredProviderFound or MissingSubscriptionRegistration, the issue might be due to the IoT Hub resource provider (Microsoft.Devices) not being registered to your subscription. [Register the **Microsoft.Devices** resource provider](data-blade:HubsExtension.RPStatusBlade.subscriptionId.$subscriptionId) then try again. <br>
[Resolve errors for resource provider registration](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors)

1. If it is already registered and still you cannot create an Iot hub, see if you can create it via Azure Portal. <br>

1. If you still can not create an IoT Hub, please wait five to fifteen minutes and try again.
