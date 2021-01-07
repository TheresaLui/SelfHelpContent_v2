<properties
    pageTitle="Unknown back-end health"
    description="Unknown back-end health"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="31"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f1"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783372"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Unknown back-end health

<!--/issueDescription-->
Application Gateway continuously probes each member in the back-end pool to monitor their health status. You can view the health of each back-end server using the [**Backend health** tab](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#back-end-health) in the Azure portal. Alternatively, you can check the detailed error message using Azure PowerShell, CLI, or REST API.

When the back-end health status can't be retrieved from Application Gateway, the status appears as **Unknown**.
<!--/issueDescription-->

## **Recommended Steps**

Follow the steps for the scenario that corresponds to your situation:

- The NSG on the Application Gateway subnet blocks inbound access to ports 65503-65534 (v1 SKU) or 65200-65535 (v2 SKU) from **Internet**. If your NSG blocks the access to these ports, you should allow inbound access from GatewayManager service tag. For more information about how to allow access, see [this article](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting#backend-health-status-unknown).
- The UDR on the Application Gateway subnet is set to the default route (0.0.0.0/0) and the next hop is not specified as **Internet**. In this case, the response packets are not reaching the destination. Make sure that internet outbound packets are allowed in your subnet by setting the next hop for 0.0.0.0/0 to **Internet**. For more information, see [this article](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting#backend-health-status-unknown).
- The default route is advertised by an ExpressRoute/VPN connection to your virtual network over BGP. In this case, the response packets are not reaching the destination. Make sure that internet outbound packets are allowed in your Application Gateway subnet either by disabling BGP propagation or adding a default route (0.0.0.0/0) with next hop as **Internet**. For more information, see [this article](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting#backend-health-status-unknown).
- The custom DNS server is configured on a virtual network that can't resolve public domain names. If you have configured a custom DNS server in your Application Gateway VNet, make sure that it can resolve to public domain names. This is required for resolving to external FQDNs like OCSP/CRL servers.
- Application Gateway is in an **Unhealthy** state. Check **Resource Health** blade to confirm if this is true. For more information, see [this article](https://docs.microsoft.com/azure/application-gateway/resource-health-overview).

## **Recommended Documents**

- [Troubleshoot backend health issues in Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting)
- [Troubleshoot unknown back-end health status issue](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting#backend-health-status-unknown)
- [Azure Application Gateway Resource Health overview](https://docs.microsoft.com/azure/application-gateway/resource-health-overview)
