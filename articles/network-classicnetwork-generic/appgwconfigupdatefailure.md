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
* If it doesn't recover from the Failed state, proceed with the support ticket
