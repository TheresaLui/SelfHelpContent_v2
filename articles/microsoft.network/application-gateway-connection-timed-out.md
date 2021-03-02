<properties 
    pageTitle="Connection timed out"
    description="Connectivity Connection Timed out"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="23"
    selfHelpType="resource"
    articleId="application-gateway-connection-timed-out-error"
    resourceTags=""
	productPesIds="15922"
	supportTopicIds="32639114"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Connectivity Issue: Connection Timed out

A connection time-out error usually occurs if the client can’t establish a TCP session with the application gateway on the requested port. This can occur for any of the following reasons:

- The client DNS can’t resolve to the application gateway's IP.
- A listener is not configured for the port on which the client is trying to establish a TCP connection.
- The listener that accepts the request doesn’t have any request routing rules associated with it.
- An NSG is blocking access to the port on which the client is sending the request.
- For the client that uses HTTPS, the connection can get rejected if the TLS version of the request is not supported by the application gateway, or the cipher suite that’s supported by the client request doesn’t match the cipher suites that are configured in [Application Gateway's SSL policy](https://docs.microsoft.com/azure/application-gateway/application-gateway-ssl-policy-overview#predefined-ssl-policy).

## **Recommended Steps**

Follow the steps below to troubleshoot:

1. Make sure that the traffic will reach the application gateway. If you are using a domain name, verify that the domain name resolves to the application gateway's IP address.
2. Make sure that your application gateway is running and is healthy according to the [Azure Resource Health criteria](https://docs.microsoft.com/azure/application-gateway/resource-health-overview).
3. Make sure that a listener is configured for the port that you’re trying to connect to. Follow [this documentation](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet) to configure a listener for the front-end port.
4. NSG or UDR could be blocking access to the ports. Check the [documentation](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet) to understand the NSG requirements, apart from allowing inbound access to the required ports. If you have a UDR configured, make sure that the application gateway can reach the client by using the configured routes.
5. If an SSL issue exists because of an SSL policy mismatch, see [Application Gateway TLS policy overview](https://docs.microsoft.com/azure/application-gateway/application-gateway-ssl-policy-overview) to learn more about the SSL policies that can be configured in Microsoft Azure Application Gateway.
