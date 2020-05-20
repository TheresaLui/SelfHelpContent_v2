<properties
	pageTitle="Connectivity Connection Timed out"
	description="Connectivity Connection Timed out"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639114"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="connectivity-connection-timedout"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Connectivity Connection Timed out

Connection timed out error when accessing Application Gateway usually occurs when the client could not establish a TCP/SSL session with the Application Gateway on the requested port due to either a listener not being configured, NSG/UDR blocking the access to the port or the domain name with which you are accessing not resolving to Application Gateway's IP address.

Check the documentation mentioned below to get guidance on how to troubleshoot these issues.

## **Recommended Documents**

* Make sure that the traffic will reach Application Gateway. For example, if you are accessing your website using a domain name, confirm that the domain name resolves to Application Gateway's IP address.
* Make sure that your Application Gateway is up and healthy using [Resource Health](https://docs.microsoft.com/azure/application-gateway/resource-health-overview)
* NSG or UDR could be blocking access to the ports. Check the [documentation](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet) to understand the NSG requirements apart from allowing inbound access to the required ports. If you have a UDR configured, make sure that Application Gateway will be able to reach the client with the routes configured.
* If there is no listener configured on the requested frontend port, follow the [documentation here](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet) to configure one and start accepting traffic.
* If there is an SSL issue due to an SSL policy mismatch, check the [documentation](https://docs.microsoft.com/azure/application-gateway/application-gateway-ssl-policy-overview) here to learn more about the SSL policies that can be configured in Application Gateway
