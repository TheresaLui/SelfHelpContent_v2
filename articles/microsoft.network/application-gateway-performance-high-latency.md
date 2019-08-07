<properties
    pageTitle="Application Gateway High latency issue"
    description="Self-help content for Performance - Application Gateway High latency"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="22"
	selfHelpType="resource"
    articleId="application-gateway-performance-high-latency"
 	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32680757"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
 />

# Application Gateway High latency
The performance and request latency of Application Gateway depends on various factors
* Client to Application Gateway latency and network performance
* Application Gateway SKU tier or size and number of instances
* Application Gateway to backend server latency and network performance
* Backend server capacity

If the performance of your application hosted behind Application Gateway is not satisfactory, follow the recommended steps below to troubleshoot.

## **Recommended Steps**

If you are experiencing high latency while trying to access your application
* Compare the timeTaken values and serverResponseLatency values in the [Application Gateway access log](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#access-log). 
* If the timeTaken value is significantly higher than the serverResponseLatency, then try increasing your Application Gateway's instance count. The number of instances can be increased from the "Configuration" tab of the Application Gateway portal or [PowerShell](https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysku?view=azps-2.5.0).
* If the above solution didn't work, try increasing the SKU to a higher size - Medium or Large for v1 (Standard and WAF). Follow the same link as mentioned above to increase the SKU size.
* If the serverResponseLatency is high, then it could be a network issue between Application Gateway and the backend servers or performance issue with the backend server.
* If you are interested in monitoring the performance of your Application Gateway, then view the [Performance metrics](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#metrics) in the portal to see the number of connections, throughput, etc.

## **Recommended Documents**
* To learn more about Application Gateway SKU sizes and throughput limits, see [here](https://docs.microsoft.com/azure/application-gateway/overview#sizing)
* [Migrate to high-performance V2 SKU of Application Gateway](https://docs.microsoft.com/azure/application-gateway/migrate-v1-v2).