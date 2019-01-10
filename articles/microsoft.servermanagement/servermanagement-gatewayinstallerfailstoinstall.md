<properties
	pageTitle="Gateway installer fails to install"
	description="What do to when the Server management tools gateway installer fails to install"
	service="microsoft.servermanagement"
	resource="gateways"
	authors="jol"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, MoonCake"
/>

# Gateway installer fails to install

## **Recommended steps**

* The GatewayService.msi installation will fail with the error “Installation ended prematurely” if you attempt to install the .msi from a remote file share. Copy the entire .zip package to a local disk on the gateway machine and install from there.

