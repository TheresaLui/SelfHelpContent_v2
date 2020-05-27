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

Connection timed out error usually occurs when the client is not able to establish a TCP session with the Application Gateway on the requested port. This can happen because of the following reasons:

- Client DNS is not able to resolve to the Application Gateway's IP
- A listener is not configured for the port on which the client is trying to establish a TCP connection
- The listener accepting the request does not have any request routing rules associated with it
- An NSG is blocking the access to the port on which the client is sending the request
- In case of HTTPS, the connection can get rejected if the TLS version of the request is not supported by the Application Gateway, and/or the cipher suite supported by the client request does not match the cipher suites configured in [Application Gateway's SSL policy](https://docs.microsoft.com/azure/application-gateway/application-gateway-ssl-policy-overview#predefined-ssl-policy)

## **Recommended Steps**

1. Check the configuration of the application gateway to ensure that there is a listener configured for the port on which the client is sending the request. If you have found that there is no listener configured on the requested front-end port, create the required listener by following the [listener configuration instructions](https://docs.microsoft.com/azure/application-gateway/configuration-overview#listeners) and ensure that this listener is associated to the relevant request routing rule.
2. Ensure that the NSG on the Application Gateway subnet is allowing inbound access to the port on which the client is making the request

If the above two steps do not resolve the issue, then proceed to file the support request.
