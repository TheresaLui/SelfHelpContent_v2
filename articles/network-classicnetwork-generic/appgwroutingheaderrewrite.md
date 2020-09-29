<properties
	pageTitle="Header and URL Rewrite Routing Issues"
	description="Header and URL Rewrite Routing Issues"
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

# Header and URL Routing Configuration Issues

Application Gateway and WAF v2 SKU supports the capability to add, remove, or update HTTP request and response headers, while the request and response packets move between the client and back-end pools. You can also rewrite URLs, query string parameters and host name. With URL rewrite and URL path-based routing, you can choose to either route requests to one of the backend pools based on the original path or the rewritten path, using the re-evaluate path map option.

It also provides you with the capability to add conditions to ensure the specified headers or URL are rewritten only when certain conditions are met. These conditions are based on the request and response information.

If you are facing any issues like the headers not getting updated, created or removed according to your configuration, follow the document on the header and URL rewrite components and verify if you have configured correctly. For configuration examples, see [common scenarios for header rewrite](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers-url#common-scenarios-for-header-rewrite) and [common scenarios for URL rewrite](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers-url#common-scenarios-for-url-rewrite) and if you are facing any issues after configuration, see [limitations](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers-url#limitations) to verify if your issue is listed there.

## **Recommended Documents**

* [Header and URL Rewrite Overview](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers-url) in Application Gateway
* Configure Header Rewrite using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/rewrite-http-headers-portal) or [PowerShell](https://docs.microsoft.com/azure/application-gateway/add-http-header-rewrite-rule-powershell)
* Configure URL Rewrite using [Azure Portal](https://docs.microsoft.com/azure/application-gateway/rewrite-url-portal)
