<properties
    pageTitle="Application Gateway High latency issue"
    description="Self-help content for Performance - Application Gateway High latency"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="34"
	selfHelpType="resource"
    articleId="application-gateway-performance-high-latency"
 	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32680757"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway High latency
The performance and request latency of Application Gateway depends on various factors

* Client to Application Gateway latency and network performance
* Application Gateway to backend server latency and network performance
* Application Gateway SKU tier or size and number of instances
* Backend server capacity

If the performance of your application hosted behind Application Gateway is not satisfactory, follow the recommended steps below to troubleshoot.

## **Recommended Steps**

When using **V2 SKU** of Application Gateway, if you observe the latency is higher than expected then perform the below steps:

* Go to the [metrics view](https://docs.microsoft.com/azure/application-gateway/application-gateway-metrics#metrics-supported-by-application-gateway-v2-sku) and analyze the **Application gateway total time** metric to verify if the latency is indeed more than expected
* If the **Application gateway total time** is more than expectation, then compare the **Client RTT **metric with the **Application gateway total time** metric. If **Client RTT** is significantly higher than the **Application gateway total time**, then this implies that the issue is with the network between the client and Application Gateway. Therefore, this is not an Application Gateway issue. If the two metrics are comparable, then perform the below step.
* Compare **Application gateway total time** with **Backend last byte response time**. If **Application gateway total time** is comparable to **Backend last byte response time**, then the issue could either be with the backend or the network between Application Gateway or the backend, and therefore, this is not an Application Gateway issue. If the **Application gateway total time** is significantly higher than the **Backend last byte response time**, then go ahead and file the ticket.

When using **V1 SKU** of Application Gateway, if you observe the latency is higher than expected then the above steps will not work as the timing-related metrics are only available on V2 SKU. Perform the below steps for V1 SKU:

- Compare the timeTaken values and serverResponseLatency values in the [Application Gateway access log](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics#access-log)
- If the timeTaken value is significantly higher than the serverResponseLatency, then try increasing your Application Gateway's instance count. The number of instances can be increased from the "Configuration" tab of the Application Gateway portal or [PowerShell](https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysku?view=azps-2.5.0).
- If the above solution didn't work, try increasing the SKU to a higher size - Medium or Large for v1 (Standard and WAF). Follow the same link as mentioned above to increase the SKU size.
- If the serverResponseLatency is high, then it could be a network issue between Application Gateway and the backend servers or performance issue with the backend server
- If you are interested in monitoring the performance of your Application Gateway, then view the [Performance metrics](https://docs.microsoft.com/azure/application-gateway/application-gateway-metrics) in the portal to see the number of connections, throughput, etc.

## **Recommended Documents**

* To learn more about Application Gateway SKU sizes and throughput limits, see [here](https://docs.microsoft.com/azure/application-gateway/overview#sizing)
* [Migrate to high-performance V2 SKU of Application Gateway](https://docs.microsoft.com/azure/application-gateway/migrate-v1-v2)
