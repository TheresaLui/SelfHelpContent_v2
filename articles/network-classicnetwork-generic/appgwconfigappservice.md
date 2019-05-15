<properties
	pageTitle="Configure Application Gateway with App Service"
	description="Configure Application Gateway with App Service"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32640602"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public"
	articleId="configure-appservice"
/>

# Configure Application Gateway with App Service
Application gateway provides a capability which allows users to override the HTTP host header in the request based on the host name of the back-end. 

This capability enables support for multi-tenant back ends such as Azure App service web apps and API management. This capability is available for both the v1 and v2 standard and WAF SKUs.

## **Recommended Documents**

* Configure Application Gateway with App Service using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/configure-web-app-portal) or [PowerShell](https://docs.microsoft.com/en-us/azure/application-gateway/create-web-app)
* [Application Gateway support for multi-tenant back ends such as App service](https://docs.microsoft.com/azure/application-gateway/application-gateway-web-app-overview) overview
* [Troubleshoot App Service redirection issues](https://docs.microsoft.com/azure/application-gateway/troubleshoot-app-service-redirection-app-service-url) with Application Gateway
