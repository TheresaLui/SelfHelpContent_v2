<properties
  pagetitle="Unable to create an IoT hub using ARM Templates, CLI, REST or Service SDK&#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner,yiygu"
  selfhelptype="Generic"
  supporttopicids="32783519"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="c011fffa-d2cf-47bb-b2df-1e2850fb7044"
  ownershipid="AzureIot_IotHub" />
# Unable to create an IoT hub using ARM Templates, CLI, REST or Service SDK

## **Recommended Steps**

1. If you got an [error](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors) similar to NoRegisteredProviderFound or MissingSubscriptionRegistration, the issue might be due to the IoT Hub resource provider (Microsoft.Devices) not being registered to your subscription. [Register the **Microsoft.Devices** resource provider](data-blade:HubsExtension.RPStatusBlade.subscriptionId.$subscriptionId) then try again. 
1. If it is already registered and still you cannot create an Iot hub, see if you can create it via Azure Portal
1. If you still cannot create an IoT Hub, please wait 15 minutes and try again