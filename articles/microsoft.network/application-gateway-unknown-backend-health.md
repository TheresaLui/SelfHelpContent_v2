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
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Unknown backend health

Application Gateway continuously probes each member in the backend pool to monitor their health status. You can view the health of each backend server using the [back-end health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) view. *Healthy* status for all backend servers is desirable. If the status is shown as *Unhealthy* or *Unknown*, then perform the below steps to troubleshoot the issue.

## **Recommended Steps**

4 out of 5 customers resolved their unknown backend health issue using the steps listed below.


1. View the [back-end health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) and check if any servers have been marked *Unhealthy* in the **Status** column. If there are unhealthy servers, then look for the reason displayed for the unhealthy state and perform the troubleshooting steps mentioned in the **Details** column.
2. If the status has been marked as *Unknown*, then ensure that NSG on the Application Gateway subnet is not blocking the access to the port, see these prerequisites for [Network security groups on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet). If you've confirmed that NSG is not blocking acccess, then ensure that UDR is not blocking the access to the port, see these prerequisites for [User-defined routes supported on the Application Gateway subnet](https://docs.microsoft.com/azure/application-gateway/configuration-overview#user-defined-routes-supported-on-the-application-gateway-subnet)

## **Recommended Documents**

- [Check back-end health using the Azure portal](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal)
- [Troubleshoot unknown backend health issues on Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting#backend-health-status-unknown)