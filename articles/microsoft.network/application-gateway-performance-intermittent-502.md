<properties
    pageTitle="Application Gateway Intermittent 502 errors"
    description="Self-help content for Performance - Application Gateway Intermittent 502 errors"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="22"
	selfHelpType="resource"
    articleId="application-gateway-performance-intermittent-502"
 	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32680758"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway Intermittent 502 errors

If you are experiencing 502 errors intermittently while accessing Application Gateway, it could be because of the following reasons:

* Application Gateway SKU tier or size and number of instances
* Application Gateway to backend server latency and network performance
* Backend server capacity and probe health

To troubleshoot the issue, follow the recommended steps below.

## **Recommended Steps**

* View the [back-end health](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#view-back-end-health-through-the-portal) and check if any servers have been marked unhealthy in the **Status** column. If there are unhealthy servers, then look for the reason displayed for the unhealthy state and perform the troubleshooting steps mentioned in the **Details** column.
* For more information on 502 troubleshooting, you can use the guided troubleshooter [here](https://support.microsoft.com/help/4504111/azure-application-gateway-with-bad-gateway-502-errors).
* If all the servers are healthy and if you are experiencing intermittent 502 errors, check the serverResponseLatency values in the [Application Gateway access log](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#access-log). 
* If the serverResponseLatency value is higher than the request timeout value configured in the HTTP settings, then try increasing it to a value more than that. It could be an issue with the backend server.
* If it is not a timeout issue, it could be due to performance of the Application Gateway or the backend server.
* Try increasing the number of instances of the Application Gateway. It can be increased from the "Configuration" tab of the Application Gateway portal or [PowerShell](https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysku?view=azps-2.5.0).
* If the above solution didn't work, try increasing the SKU to a higher size - Medium or Large for v1 (Standard and WAF). Follow the same link as mentioned above to increase the SKU size.
* If the issue is not with Application Gateway performance, check for any performance issues with the backend server.

## **Recommended Documents**

- [Check throughput limits for application gateway](https://azure.microsoft.com/documentation/articles/application-gateway-introduction/).
- [Migrate to high-performance V2 SKU of Application Gateway](https://docs.microsoft.com/azure/application-gateway/migrate-v1-v2).
- [Troubleshoot 502 Bad Gateway error](https://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
- Learn more about [Performance metrics](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#metrics)
