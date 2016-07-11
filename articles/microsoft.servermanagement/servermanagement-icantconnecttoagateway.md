<properties
	pageTitle="I can’t connect to a gateway"
	description="I can't connect to a Server management tools gateway"
	service="microsoft.servermanagement"
	resource="gateways"
	authors="jol"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I can’t connect to a gateway

## **Recommended steps**
To resolve common issues, try one or more of the following methods.

* Make sure the Health status on the gateway blade is displayed as “OK” and there aren’t any additional errors or warnings displayed.
* Log on to the gateway machine and make sure it can connect to the public internet.
* In the Windows Start menu, type and run “services.msc” to launch the Services MMC snap-in. Make sure the “Server management tools gateway” service is running. Also try restarting the service.
* You can try reinstalling the gateway deployment package. On the gateway machine, go to “Programs and Features” and uninstall “Server management tools gateway”. Generate a gateway deployment package, download and install it on the gateway machine.

## **Recommended documents**
[Introducing Server management tools](https://blogs.technet.microsoft.com/nanoserver/2016/02/09/introducing-server-management-tools/)
