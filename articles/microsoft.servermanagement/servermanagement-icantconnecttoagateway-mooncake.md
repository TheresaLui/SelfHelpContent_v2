<properties
    pageTitle="I can’t connect to a gateway"
    description="I can't connect to a Server management tools gateway"
    service="microsoft.servermanagement"
    resource="gateways"
    authors="jol"
    ms.author="jol"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="e6a04dcf-b2fe-4121-9df4-41a716d48c2f"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# I can’t connect to a gateway

## **Recommended Steps**

To resolve common issues, try one or more of the following:

* Make sure the Health status on the gateway blade is displayed as “OK” with no additional errors or warnings displayed
* Log on to the gateway machine and make sure it can connect to the public internet
* Run “services.msc” to launch the Services MMC snap-in and make sure the “ServerManagementToolsGateway” service is running.
* Restart the service
* Make sure the system date/time on the gateway machine is correct. Gateway authorization will fail if the system time between the gateway and the Server management tools Azure service differ by more than 15 minutes.
* You can try reinstalling the gateway deployment package. On the gateway machine, go to “Programs and Features” and uninstall “Server management tools gateway”. [Generate a gateway deployment package](data-blade:Microsoft_Azure_RSMT.GatewaySetupBlade), download and install it on the gateway machine.
