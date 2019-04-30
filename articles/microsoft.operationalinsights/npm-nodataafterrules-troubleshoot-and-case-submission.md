<properties
	pageTitle="I installed NPM and setup rules but I do not see any data"
	description="I installed NPM and setup rules  but I do not see any data"
	service="microsoft.operationalinsights"
	resource="operationalinsightsaccounts"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32626098"
	resourceTags=""
	productPesIds="15725"
	cloudEnvironments="public,fairfax"
/>

# No monitoring data in NPM

## **Recommended steps**

*  To check if NPM is receiving any data, run the below mentioned query in LogAnalytics for your workspace <br> 

```
NetworkMonitoring | take 5
```

* To check if Performance Monitor tests are recording data, run the below mentioned query in LogAnalytics for your workspace <br> 

``` 
NetworkMonitoring | where SubType == "SubNetwork"
```

* To check if Service Connectivity Monitor tests are recording data, run the below mentioned query in LogAnalytics for your workspace <br> 

```
NetworkMonitoring | where SubType == "SubNetwork" 
```

* To check if Express Route Monitor circuits are recording data, run the below mentioned query in LogAnalytics for your workspace <br> 

```
NetworkMonitoring 
| where SubType == "ExpressRouteCircuitUtilization" 
| project CircuitName
```

* To check if Express Route Monitor peerings are recording data, run the below mentioned query in LogAnalytics for your workspace <br>  

```
NetworkMonitoring 
| where SubType == "ExpressRoutePeeringUtilization"
| project CircuitName,PeeringName
```


## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)

