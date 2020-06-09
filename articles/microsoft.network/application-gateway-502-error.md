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
    supportTopicIds="32573483,32680993"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Bad Gateway Error (502)

Bad Gateway Error (502) occurs when the Application Gateway does not receive a valid response from the backend application. 9 out of 10 times this happens when the application gateway's health probe detects the backend servers to be unhealthy and takes them out of rotation until they are found healthy again. If all the instances of BackendAddressPool are unhealthy, then the application gateway doesn't have any back-end to route user request to, resulting in Bad Gateway Error (502).

## **Recommended Steps**

1. View the [back-end health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) and check if any servers have been marked unhealthy in the **Status** column. If there are unhealthy servers, then look for the reason displayed for the unhealthy state mentioned in the **Details** column. After confirming the reason for the backend being unhealthy, perform the troubleshooting steps mentioned in this article: [Causes for 502 errors with Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
2. If the backend servers are shown as healthy, then proceed to file the support ticket

## **Recommended Documents**

- [Troubleshoot 502 errors with Application Gateway using guided troubleshooter](https://support.microsoft.com/help/4504111/azure-application-gateway-with-bad-gateway-502-errors)

