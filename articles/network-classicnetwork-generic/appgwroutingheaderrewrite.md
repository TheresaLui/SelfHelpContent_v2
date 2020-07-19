<properties
	pageTitle="Header Rewrite Routing Issues"
	description="Header Rewrite Routing Issues"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32641400"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="routing-header-rewrite"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Header Rewrite Routing Issues

Application Gateway allows you to add, remove, or update HTTP request and response headers while the request and response packets move between the client and back-end pools. And it allows you to add conditions to ensure that the specified headers are rewritten only when certain conditions are met.

If you are facing any issues like the headers not getting updated, created or removed according to your configuration, follow the document on the header rewrite components and verify if you have configured correctly. For configuration examples, see [common scenarios](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers#common-scenarios) and if you are facing any issues after configuration, see [limitations](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers#limitations) to verify if your issue is listed there.

## **Recommended Documents**

* [Header Rewrite Overview](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers) in Application Gateway
* Configure Header Rewrite using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers-portal) or [PowerShell](https://docs.microsoft.com/azure/application-gateway/add-http-header-rewrite-rule-powershell)
