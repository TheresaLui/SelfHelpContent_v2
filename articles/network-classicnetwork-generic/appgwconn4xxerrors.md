<properties
	pageTitle="Connectivity 4xx Errors"
	description="Connectivity 4xx Errors"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639113"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="connectivity-4xx-errors"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Connectivity 4xx Errors

4xx errors are usually client side errors and can occur due to one or more of the following reasons:

* Backend Server returns 4xx error, for example, if the requested page is not found on the server, it will return a 404 Page Not Found error
* Application Gateway does not have a rule with basic listener and the hostname of the request does not match with any multi-site listeners
* 403 error due to Web Application Firewall (WAF) blocking the request
* 400 Bad Request due to a malformed request by the client

You can troubleshoot the issue by directly accessing the server and check if it returns the same 4xx error or using the Application Gateway access logs to find the same. Check the documentation mentioned below to get guidance on how to enable and analyze Application Gateway and WAF logs.

## **Recommended Documents**

* [Diagnostics and Logging](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#diagnostic-logging) in Application Gateway
* Web Application Firewall [reporting and logs](https://docs.microsoft.com/azure/application-gateway/waf-overview#logging)
