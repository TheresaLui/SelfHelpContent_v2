<properties
	pageTitle="I installed NPM and setup monitoring in Express Route Monitor but I do not see any data in the dashboard"
	description="I installed NPM and setup monitoring in Express Route Monitor  but I do not see any data in the dashboard"
	service="microsoft.network"
	resource="networkWatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="7"
	selfHelpType="generic"
	supportTopicIds="32606433"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="npm-nodataforermrule-troubleshoot-and-case-submission"
	ownershipId="CloudNet_NetAnalytics"
/>

# No monitoring data in NPM for Express Route Monitor

## **Recommended Steps**

* To check if Express Route Monitor circuits are recording data, run the below mentioned query in Log Analytics for your workspace: <br>

```
NetworkMonitoring
| where SubType == "ExpressRouteCircuitUtilization"
| project CircuitName
```

* To check if Express Route Monitor peerings are recording data, run the below mentioned query in Log Analytics for your workspace: <br>

```
NetworkMonitoring
| where SubType == "ExpressRoutePeeringUtilization"
| project CircuitName,PeeringName
```

*  To check if NPM is receiving any data for a specific circuit, run the below mentioned query in Log Analytics for your workspace:

```
NetworkMonitoring
| where CircuitName == "<<Your circuit name>>"
| take 5
```

*  To check if NPM is receiving any data for a specific peering, run the below mentioned query in Log Analytics for your workspace:

```
NetworkMonitoring
| where CircuitName = "<<Your circuit name>>" && PeeringName == "<<your peering name>>"
| take 5
```

* It takes NPM about 30 mins to start showing data after initial setup <br>
* Check circuit and peering metrics in Azure Monitor to see if circuit and peering are receiving any data. If there is no data in NPM and in Azure monitor, reach out to the Express Route team.


## **Recommended Documents**

* [Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
* [Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
* [Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
* [Learn more about NPM Monitoring Alerts](https://docs.microsoft.com/azure/expressroute/expressroute-monitoring-metrics-alerts)
