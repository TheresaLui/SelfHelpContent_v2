<properties
	pageTitle="Connectivity 502 Error"
	description="Connectivity 502 Error"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32573483"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cb9a55ba-84d0-430b-a741-f5b65a13b149"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Connectivity 502 Error

502 Bad Gateway error can happen due to various reasons. Most commonly, it could be one of the following:

* Backend servers failing to respond to health probes or response status code or body mismatch from what is configured
* Certificate mismatch for End-to-End SSL scenario, which may lead to probe failures
* Backend servers timing out for requests sent from Application Gateway
* Request being sent to an empty backend pool
* A basic rule has been listed on top of the multi-site rules which catches all the requests and routes them to unintended backend pool

You can troubleshoot the issue using the [guided troubleshooting document](https://support.microsoft.com/help/4504111/azure-application-gateway-with-bad-gateway-502-errors) or going through the recommended documentation for more details.

## **Recommended Documents**

* Troubleshoot [Bad Gateway Errors (502)](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502) in Application Gateway
