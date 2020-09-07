<properties
	pageTitle="I installed NPM and setup monitoring in Performance Monitor but I do not see any data in the dashboard"
	description="I installed NPM and setup monitoring in Performance Monitor  but I do not see any data in the dashboard"
	service="microsoft.network"
	resource="networkWatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32606442"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="MoonCake"
	articleId="npm-nodataforpmrule-troubleshoot-and-case-submission-mooncake"
	ownershipId="CloudNet_NetAnalytics"
/>

# NPM for Performance Monitor

## **Recommended Steps**

*  To check if NPM is receiving any data for a given network, run the below mentioned query in Log Analytics for your workspace:

```
NetworkMonitoring
| where SubType == "Network"
| where SourceNetwork == "<<Your Network name>>"
```

*  To check if NPM is receiving any data for a given subnetwork, run the below mentioned query in Log Analytics for your workspace:

```
NetworkMonitoring
| where SubType == "SubNetwork"
| where SourceSubNetwork == "<<Your SubNetworkNetwork IP>>"
```

*  To check if NPM is receiving any data for a given rule, run the below mentioned query in Log Analytics for your workspace:

```
NetworkMonitoring
| where RuleName == "<<Your rule name>>"
```

* It takes NPM about 30 mins to start showing data after the initial setup


## **Recommended Documents**

* [Learn more about NPM agent](https://docs.azure.cn/azure-monitor/platform/agent-windows)
* [Learn more about NPM](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Performance Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Service Connectivity Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Express Route Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-expressroute)
* [Learn more about NPM Frequently asked questions](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-faq)
