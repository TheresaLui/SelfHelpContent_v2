<properties
	pageTitle="I can't create an IoT hub"
	description="I can't create an IoT hub"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds="32596670"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Unable to create an IoT hub

## **Recommended steps**

1. If you got an error similar to `NoRegisteredProviderFound` or `MissingSubscriptionRegistration`, the issue might be due to the IoT Hub resource provider (Microsoft.Devices) not registered to your subscription. Follow the guide below to register the **Microsoft.Devices** resource provider then try again. <br>
[Resolve errors for resource provider registration](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors)

1. If it is already registered and still you cannot create an Iot hub, see if you can create it via Azure CLI or PowerShell. <br>
[Create an IoT hub using Azure CLI](https://docs.microsoft.com/azure/iot-hub/iot-hub-create-using-cli)<br>
[Create an IoT hub using Azure PowerShell](https://docs.microsoft.com/azure/iot-hub/iot-hub-create-using-powershell)