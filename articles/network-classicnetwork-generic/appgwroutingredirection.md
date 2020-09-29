<properties
	pageTitle="HTTP Redirection"
	description="HTTP Redirection"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32640608"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="http-redirection"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# HTTP Redirection

You can use Application Gateway to redirect traffic. It has a generic redirection mechanism which allows for redirecting traffic received at one listener to another listener or to an external site.

Also, redirection can occur due to backend application configuration. For example, you might see the App Service getting exposed in the browser when the backend server is an Azure App Service and if it has redirection enabled. Check the troubleshooting document below for guidance on debugging the redirection issue.

## **Recommended Documents**

* [Troubleshoot App Service redirection issues](https://docs.microsoft.com/azure/application-gateway/troubleshoot-app-service-redirection-app-service-url) with Application Gateway
* [HTTP Redirection](https://docs.microsoft.com/azure/application-gateway/redirect-overview) overview on Application Gateway
