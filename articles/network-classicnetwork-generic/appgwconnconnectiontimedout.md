<properties
	pageTitle="Connectivity Connection Timed out"
	description="Connectivity Connection Timed out"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639114"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public"
	articleId="connectivity-connection-timedout"
/>

# Connectivity Connection Timed out

Connection timed out error when accessing Application Gateway usually occurs when the client could not establish a TCP session with the Application Gateway on the requested port due to either a listener not being configured or NSG/UDR blocking the access to the port.

Check the documentation mentioned below to get guidance on how to troubleshoot these issues.

## **Recommended Documents**

* NSG or UDR could be blocking access to the ports. Check the [documentation](https://docs.microsoft.com/en-us/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet) to understand the NSG requirements apart from allowing inbound access to the required ports.
* If there is no listener configured on the requested frontend port, follow the [documentation here](https://docs.microsoft.com/en-us/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet) to configure one and start accepting traffic.
