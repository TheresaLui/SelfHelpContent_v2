<properties
	pageTitle="microsoft azure web apps (azurewebsites.net) configuration"
	description="microsoft azure web apps (azurewebsites.net) configuration"
	service="microsoft.network"
	resource="trafficmanagerprofiles"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32336442"
	resourceTags=""
	productPesIds="15400"
	cloudEnvironments="public"
/>

# microsoft azure web apps (azurewebsites.net) configuration
## **Recommended steps**
Only Web Apps at the "Standard" SKU or above are eligible for use with Traffic Manager. Calls to Traffic Manager to add a Web App of a lower SKU will fail. Downgrading the SKU of an existing Web App will result in Traffic Manager no longer sending traffic to that Web App, and the endpoint may be removed from Traffic Manager.
For more information please review:[Traffic Manager endpoints](https://azure.microsoft.com/documentation/articles/traffic-manager-endpoint-types/)

## **Recommended documents**
[Controlling Azure Web App with Traffic Manager](https://azure.microsoft.com/documentation/articles/web-sites-traffic-manager/)<br>


