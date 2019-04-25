<properties 
    pageTitle="Unknown backend health"
    description="Unknown backend health with Application Gateway"
    infoBubbleText="Common solution article for instructions on how to troubleshoot unknown backend issues with Application Gateway."
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-unknown-backend-health"
    diagnosticScenario="ApplicationGatewayUnknownBackendHealth"
    supportTopicIds="32639117"
    cloudEnvironments="public"
 />

# Unknown backend health

While invoking the backend health API, you can get the status as Unknown due to one of the following reasons:

- Application Gateway Subnet has an NSG/UDR blocking access to the ports 65503-65534 inbound on V1 SKU and 65200-65534 on V2 SKU. To ensure that an NSG or UDR is not blocking the access to the port, see these prerequisites.

  - [Network security groups on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet). Additionally, ensure that the NSG is allowing inbound access to the required ports.
  - [User-defined routes supported on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#user-defined-routes-supported-on-the-application-gateway-subnet)
  
- You have an ExpressRoute/VPN connection with default route (0.0.0.0/0) enabled which will force the API responses to your on-premises network.

## **Recommended Documents**

[View health of the Application Gateway's backend instances](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal)