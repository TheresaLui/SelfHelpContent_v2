<properties
    pageTitle="I'm encountering performance issues"
    description="Self-help content for Performance-related issues in Application Gateway"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="23"
	selfHelpType="resource"
    articleId="application-gateway-performance-mooncake"
 	resourceTags=""
	productPesIds=""
    supportTopicIds=""
    cloudEnvironments="MoonCake"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Performance issue

If your issue is related to 502 errors, high latency, performance monitoring or slow configuration update, then perform the troubleshooting steps mentioned below specific to your issue. If it is a different issue, then please go ahead and file the support request.

## **Recommended Steps**

- **502 errors:** If you are experiencing 502 errors while trying to access the application, then navigate one step back to the *Basics* tab by clicking the **<<Previous: Basics** button at the bottom of the page and then select *Connectivity* in the *Problem type* dropdown. In the *Problem subtype* dropdown, select *502 errors* and proceed ahead to view the troubleshooting instructions.
- **High latency**: If you are experiencing high latency while trying to access your application, then compare the timeTaken values and serverResponseLatency values in the [Application Gateway access log](https://docs.azure.cn/application-gateway/application-gateway-diagnostics#access-log). If the values are higher than expected, then go ahead and file a support request. If not, then this may be a WAN issue.
- **Monitor performance**: If you are interested in monitoring the performance of your Application Gateway, then view the [Performance metrics](https://docs.azure.cn/application-gateway/application-gateway-diagnostics#metrics) in the portal to see the number of connections, throughput, etc.
- **Configuration update taking too long**: If the configuration update is taking too long, then navigate one step back to the *Basics* tab by clicking the **<<Previous: Basics** button at the bottom of the page and then select *Configuration and Setup* in the *Problem type* dropdown. In the *Problem subtype* dropdown, select *Configuration update failure* and proceed ahead to view the troubleshooting instructions.

## **Recommended Documents**

- [Check throughput limits for application gateway](https://docs.azure.cn/application-gateway/overview).