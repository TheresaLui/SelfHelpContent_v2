<properties 
    pageTitle="Connection timed out"
    description="Connectivity Connection Timed out"
    infoBubbleText="Common solution article for instructions on how to troubleshoot connection timed-out errors with Application Gateway."
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder=""
	selfHelpType="resource"
    articleId="application-gateway-connection-timed-out-error"
    diagnosticScenario="ApplicationGatewayConnectionTimedOutError"
    supportTopicIds="32639114"
    cloudEnvironments="public"
 />

# Connectivity Issue: Connection Timed out

Connection timed out error usually occurs when the client is not able to establish a TCP session with the Application Gateway on the requested port. This can happen because of the following reasons:

- A listener is not configured for the port on which the client is trying to establish a TCP connection
- An NSG/UDR is blocking the access to the port

## **Recommended Documents**

- If you have found that there is no listener configured on the requested front-end port, create the required listener by following the [listener configuration instructions](https://docs.microsoft.com/azure/application-gateway/configuration-overview#listeners)
- To ensure that an NSG or UDR is not blocking the access to the port, see these prerequisites:

    - [Network security groups on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet). Additionally, ensure that the NSG is allowing inbound access to the required ports.
    - [User-defined routes supported on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#user-defined-routes-supported-on-the-application-gateway-subnet)
