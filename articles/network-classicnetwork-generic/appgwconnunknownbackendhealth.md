<properties
	pageTitle="Unknown Backend Health"
	description="Unknown Backend Health"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639116"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="unknown-backend-health"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Unknown Backend Health

Application Gateway provides the users the ability to check backend server health status using the Azure Portal, using PowerShell, CLI commands and using REST API.

While invoking the backend health API, you might see the status as Unknown sometimes due to one of the following reasons.

* Application Gateway Subnet has an NSG/UDR blocking access to the ports 65503-65534 inbound on V1 SKU and 65200-65534 on V2 SKU.
* You have an ExpressRoute/VPN connection with default route (0.0.0.0/0) enabled which will force the API responses to your on-premises network.

If you are not able to view your backend health, it could be a transient issue. Try it again for a couple of times. If it is still not getting resolved, follow the guidelines in the documentation mentioned below.

## **Recommended Documents**

* [Unknown Backend Health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) in Application Gateway
* [Verifying Backend Health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) in Application Gateway
