<properties
	pageTitle="Too Many Redirects Connectivity Error"
	description="Too Many Redirects Connectivity Error"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639115"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="connectivity-too-many-redirects"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Too Many Redirects Connectivity Error

Too many redirects error can occur when accessing Application Gateway due to one or more of the following reasons:

* Backend Server has a redirection loop
* Application Gateway is configured with SSL offload but backend server can accept only HTTPS requests so it redirects the client to use only HTTPS

You can troubleshoot the issue by directly accessing the server and check if the behavior is the same or using the Application Gateway access logs to find the same. Check the documentation mentioned below to get guidance on how to enable and analyze Application Gateway logs.

## **Recommended Documents**

* [Diagnostics and Logging](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#diagnostic-logging) in Application Gateway
