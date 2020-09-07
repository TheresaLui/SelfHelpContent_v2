<properties 
    pageTitle="Unknown backend health"
    description="Unknown backend health with Application Gateway"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="27"
    selfHelpType="resource"
    articleId="application-gateway-unknown-backend-health-mooncake"
	resourceTags=""
	productPesIds=""
    supportTopicIds=""
    cloudEnvironments="MoonCake"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Unknown backend health

Application Gateway continuously probes each member in the backend pool to monitor their health status. You can view the health of each backend server using the [back-end health](https://docs.azure.cn/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) view. *Healthy* status for all backend servers is desirable. If the status is shown as *Unhealthy* or *Unknown*, then perform the below steps to troubleshoot the issue.

## **Recommended Steps**

1. View the [back-end health](https://docs.azure.cn/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) and check if any servers have been marked *Unhealthy* in the **Status** column. If there are unhealthy servers, then look for the reason displayed for the unhealthy state and perform the troubleshooting steps mentioned in the **Details** column.
2. If the status has been marked as *Unknown*, then ensure that NSG on the Application Gateway subnet is not blocking the access to the port, see these prerequisites for [Network security groups on the Application Gateway subnet](https://docs.azure.cn/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet). If you've confirmed that NSG is not blocking acccess, then ensure that UDR is not blocking the access to the port, see these prerequisites for [User-defined routes supported on the Application Gateway subnet](https://docs.azure.cn/application-gateway/configuration-overview#user-defined-routes-supported-on-the-application-gateway-subnet)