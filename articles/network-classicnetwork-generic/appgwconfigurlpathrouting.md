<properties
	pageTitle="Configure URL Path-Based Routing"
	description="Configure URL Path-Based Routing"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32582830"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8eeda772-6f4c-4aa1-b003-7092225d94c1"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configure URL Path-Based Routing

URL Path Based Routing allows you to route traffic to back-end server pools based on URL Paths of the request. For example, it can be configured so where requests to Application Gateway with path "/images" can be routed to backend pool A and requests with path "/videos" can be routed to backend pool B.

## **Recommended Documents**

* Configure Path based routing for Application Gateway using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/application-gateway-create-url-route-portal) or [PowerShell](https://docs.microsoft.com/azure/application-gateway/tutorial-url-route-powershell)
* [URL path based routing](https://docs.microsoft.com/azure/application-gateway/url-route-overview) overview on Application Gateway
