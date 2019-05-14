<properties
	pageTitle="Configuration Update Failure"
	description="Configuration Update Failure"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639110"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public"
	articleId="xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
/>

# Configuration Update Failure
When you make any changes to the Application Gateway and the update takes long time (more than an hour) to finish or if the Application Gatweway shows up as Failed in provisioning state, try one of the following recommended steps.

## **Recommended steps**
* Using Azure PowerShell try executing a [GetApplicationGateway](https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway?view=azps-1.7.0) and a [SetApplicationGateway](https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway?view=azps-1.7.0) in sequence and check if it recovers from the Failed state.
* Try [Stopping](https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway?view=azurermps-6.13.0) and [Starting](https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway?view=azurermps-6.13.0) Application Gateway to verify if it recovers from the Failed state (**Note:** If it is a V1 SKU gateway, since the IP address is dynamic, you will lose the existing public IP and a new one will be assigned post restart)
* If it doesn't recover from the Failed state,  proceed with the support ticket