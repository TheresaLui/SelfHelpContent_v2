<properties 
    pageTitle="I'm encountering Bad Gateway Error (502)"
    description="Bad Gateway Error (502)"    
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="20"
    selfHelpType="resource"
    articleId="application-gateway-502-error"
    resourceTags=""
	productPesIds="15922"
    supportTopicIds="32573483"
    cloudEnvironments="public"
 />

# Bad Gateway Error (502)

Bad Gateway Error (502) occurs when the Application Gateway does not receive a valid response from the backend application. 9 out of 10 times this happens when the application gateway's health probe detects the backend servers to be unhealthy and takes them out of rotation until they are found healthy again. If all the instances of BackendAddressPool are unhealthy, then the application gateway doesn't have any back-end to route user request to, resulting in Bad Gateway Error (502).

## Recommended Steps

1. View the [back-end health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) and check if any servers have been marked unhealthy in the **Status** column. If there are unhealthy servers, then look for the reason displayed for the unhealthy state and perform the troubleshooting steps mentioned in the **Details** column.
2. If the backend servers are shown as healthy, then proceed to file the support ticket

If it is verified that the backend is healthy, then perform the steps in links below to troubleshoot the issue.

## **Recommended Documents**

The bad gateway error (502) can happen due to one or more of the following issues:

- [NSG, UDR or Custom DNS is blocking access to backend pool members](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#network-security-group-user-defined-route-or-custom-dns-issue)
- [Back-end VMs or instances of virtual machine scale set are not responding to the default health probe](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-default-health-probe)
- [Invalid or improper configuration of custom health probes](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#problems-with-custom-health-probe)
- [Request time-out or connectivity issues with user requests](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#request-time-out)
- [Empty backend pool](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#empty-backendaddresspool)
- [Unhealthy instances in the backend pool](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502#unhealthy-instances-in-backendaddresspool)
