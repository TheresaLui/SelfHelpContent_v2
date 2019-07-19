<properties 
    pageTitle="Unknown backend health"
    description="Unknown backend health with Application Gateway"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="21"
    selfHelpType="resource"
    articleId="application-gateway-unknown-backend-health"
	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32639116"
    cloudEnvironments="public"
 />

# Unknown backend health

While invoking the backend health API, you can get the status as Unknown due to one of the following reasons:

- Application Gateway Subnet has an NSG/UDR blocking access to the ports 65503-65534 inbound on V1 SKU and 65200-65534 on V2 SKU
- You have an ExpressRoute/VPN connection with default route (0.0.0.0/0) enabled which will force the API responses to your on-premises network

## Recommended Steps

1. View the [back-end health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) and check if any servers have been marked *Unhealthy* in the **Status** column. If there are unhealthy servers, then look for the reason displayed for the unhealthy state and perform the troubleshooting steps mentioned in the **Details** column.
2. If the status has been marked as *Unknown*, then ensure that an NSG is not blocking the access to the port, see these prerequisites for [Network security groups on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet). Additionally, ensure that the NSG is allowing inbound access to the required ports.
3. If the status has been marked as *Unknown*, then ensure that UDR is not blocking the access to the port, see these prerequisites for [User-defined routes supported on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#user-defined-routes-supported-on-the-application-gateway-subnet)