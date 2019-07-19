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
    cloudEnvironments="public"
 />

# Connectivity Issue: Connection Timed out

Connection timed out error usually occurs when the client is not able to establish a TCP session with the Application Gateway on the requested port. This can happen because of the following reasons:

- Client DNS is not able to resolve to the Application Gateway's IP
- Configuration issues:
  - A listener is not configured for the port on which the client is trying to establish a TCP connection.
  - The listener accepting the request does not have any request routing rules associated with it.
- An NSG/UDR is blocking the access to the port.
- In case of HTTPS connected, if the connection is rejected because of:
  - The TLS version of the request is not supported by the Application Gateway.
  - The cipher suite supported by the client request does not match the cipher suites configured in [Application Gateway's SSL policy](https://docs.microsoft.com/azure/application-gateway/application-gateway-ssl-policy-overview#predefined-ssl-policy).

## Recommended Steps

- If you have found that there is no listener configured on the requested front-end port, create the required listener by following the [listener configuration instructions](https://docs.microsoft.com/azure/application-gateway/configuration-overview#listeners)
- To ensure that an NSG or UDR is not blocking the access to the port, see these prerequisites:

    - [Network security groups on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet). Additionally, ensure that the NSG is allowing inbound access to the required ports.
    - [User-defined routes supported on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#user-defined-routes-supported-on-the-application-gateway-subnet)
