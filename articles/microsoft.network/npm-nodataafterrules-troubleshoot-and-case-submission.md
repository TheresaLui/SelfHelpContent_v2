<properties
	pageTitle="I installed NPM and setup rules but I do not see any data"
	description="I installed NPM and setup rules  but I do not see any data"
	service="microsoft.network"
	resource="networkwatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32606425"
	resourceTags=""
	productPesIds="16160"
    articleId="npm-nodataafterrules-troubleshoot-and-case-submission-nw"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="CloudNet_NetAnalytics"
/>

# No monitoring data in NPM

## **Recommended Steps**

*  To check if NPM is receiving any data, run the below mentioned query in LogAnalytics for your workspace: <br> 

```
NetworkMonitoring | take 5
```

* To check if Performance Monitor tests are recording data, run the below mentioned query in LogAnalytics for your workspace: <br> 

``` 
NetworkMonitoring | where SubType == "SubNetwork"
```

* To check if Service Connectivity Monitor tests are recording data, run the below mentioned query in LogAnalytics for your workspace: <br> 

```
NetworkMonitoring | where SubType == "SubNetwork" 
```

* To check if Express Route Monitor circuits are recording data, run the below mentioned query in LogAnalytics for your workspace: <br> 

```
NetworkMonitoring 
| where SubType == "ExpressRouteCircuitUtilization" 
| project CircuitName
```

* To check if Express Route Monitor peerings are recording data, run the below mentioned query in LogAnalytics for your workspace: <br>  

```
NetworkMonitoring 
| where SubType == "ExpressRoutePeeringUtilization"
| project CircuitName,PeeringName
```


## **Recommended Documents**

* [Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
* [Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
* [Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)