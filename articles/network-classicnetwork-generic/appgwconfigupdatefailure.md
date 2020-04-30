<properties
	pageTitle="Configuration Update Failure"
	description="Configuration Update Failure"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639110"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="config-update-failure"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configuration Update Failure
When you make any changes to the Application Gateway and the update takes long time (more than an hour) to finish or if the Application Gatweway shows up as Failed in provisioning state, be assured that your Application Gateway is still running and serving the client requests but you cannot make any changes to the configuration until it is recovered from the failed state.

To recover an Application Gateway from failed state, try one of the following recommended steps.

## **Recommended Steps**

* Using Azure PowerShell try executing the [Get Application Gateway](https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgateway?view=azps-1.7.0) and a [Set Application Gateway](https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgateway?view=azps-1.7.0) commands in sequence and check if it recovers from the Failed state
* Otherwise, try [Stopping](https://docs.microsoft.com/powershell/module/azurerm.network/stop-azurermapplicationgateway?view=azurermps-6.13.0) and [Starting](https://docs.microsoft.com/powershell/module/azurerm.network/start-azurermapplicationgateway?view=azurermps-6.13.0) Application Gateway to verify if it recovers from the Failed state (**Note:** If it is a V1 SKU gateway, since the IP address is dynamic, you will lose the existing public IP and a new one will be assigned post restart)
* If it doesn't recover from the Failed state, proceed with the support ticket
