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
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="configure-appservice"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configure Application Gateway with App Service
Since app service is a multi-tenant service instead of a dedicated deployment, it uses host header in the incoming request to resolve the request to the correct app service endpoint. Since the domain name of the Application Gateway fronting the app service is different from the app service's domain name, `Pick host name from backend address` switch is required to be enabled to override the original host header in the request with the host name of the app service back-end, when the request is routed from the Application Gateway to the backend. 

## **Recommended Steps**

1. If you want to configure Application Gateway with app service as backend, see [How to configure app service with Application Gateway](https://docs.microsoft.com/azure/application-gateway/configure-web-app-portal)
2. If you have already configured your app service with Application Gateway and are experiencing issues, then see [Troubleshoot app service issues with Application Gateway](https://docs.microsoft.com/azure/application-gateway/troubleshoot-app-service-redirection-app-service-url)

If the instructions in the above 2 steps do not resolve your issue, then proceed to file the support request.