<properties
	pageTitle="I installed NPM and setup rules but I do not see any data"
	description="I installed NPM and setup rules  but I do not see any data"
	service="microsoft.network"
	resource="networkwatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="31"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
    articleId="npm-nodataafterrules-troubleshoot-and-case-submission-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="CloudNet_NetAnalytics"
/>

# No monitoring data in NPM

## **Recommended Steps**

*  To check if NPM is receiving any data, run the below mentioned query in LogAnalytics for your workspace:

    ```
    NetworkMonitoring | take 5
    ```

* To check if Performance Monitor tests are recording data, run the below mentioned query in LogAnalytics for your workspace:

    ``` 
    NetworkMonitoring | where SubType == "SubNetwork"
    ```

* To check if Service Connectivity Monitor tests are recording data, run the below mentioned query in LogAnalytics for your workspace:

    ```
    NetworkMonitoring | where SubType == "SubNetwork" 
    ```

* To check if Express Route Monitor circuits are recording data, run the below mentioned query in LogAnalytics for your workspace:

    ```
    NetworkMonitoring 
    | where SubType == "ExpressRouteCircuitUtilization" 
    | project CircuitName
    ```

* To check if Express Route Monitor peerings are recording data, run the below mentioned query in LogAnalytics for your workspace:

    ```
    NetworkMonitoring 
    | where SubType == "ExpressRoutePeeringUtilization"
    | project CircuitName,PeeringName
    ```


## **Recommended Documents**

* [Learn more about NPM agent](https://docs.azure.cn/azure-monitor/platform/agent-windows)
* [Learn more about NPM](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Performance Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Service Connectivity Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Express Route Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-expressroute)
* [Learn more about NPM Frequently asked questions](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-faq)