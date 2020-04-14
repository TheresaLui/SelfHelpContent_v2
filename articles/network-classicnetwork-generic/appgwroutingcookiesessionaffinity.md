<properties
	pageTitle="Cookie Based Session Affinity"
	description="Cookie Based Session Affinity"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32640605"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cookie-based-affinity"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Cookie Based Session Affinity

Application Gateway cookie based affinity enables the application gateway to direct subsequent traffic from a user session to the same server for processing. This is achieved by the client setting a cookie sent by the Application Gateway in subsequent requests in the same session.

Make sure that the clients are setting the affinity cookie while sending subsequent requests so that the sticky sessions can be maintained.


## **Recommended Documents**

* [Troubleshoot](https://support.microsoft.com/help/4033827/troubleshooting-azure-application-gateway-session-affinity-issues) Application Gateway session affinity issues <br />
* [Cookie Based Session affinity](https://docs.microsoft.com/azure/application-gateway/configuration-overview#cookie-based-affinity) overview on Application Gateway
