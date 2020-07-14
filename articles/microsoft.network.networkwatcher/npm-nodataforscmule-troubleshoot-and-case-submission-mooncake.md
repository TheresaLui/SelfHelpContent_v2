<properties
	pageTitle="I installed NPM and setup monitoring in Service Connectivity Monitor but I do not see any data in the dashboard"
	description="I installed NPM and setup rules but I do not see any data for my rule"
	service="microsoft.network"
	resource="networkWatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32606443"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="MoonCake"
	articleId="npm-nodataforscmule-troubleshoot-and-case-submission-mooncake"
	ownershipId="CloudNet_NetAnalytics"
/>

# No monitoring data in NPM for a specific rule

## **Recommended Steps**

*  To check if NPM is receiving any data for a specific test, run the below mentioned query in LogAnlaytics for your workspace:

```
NetworkMonitoring
| where TestName == "<<Your Service Connectivity Monitor test name>>"
| take 5
```

* It takes NPM about 30 mins to start showing data after initial setup

## **Recommended Documents**

* [Learn more about NPM agent](https://docs.azure.cn/azure-monitor/platform/agent-windows)
* [Learn more about NPM](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Performance Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Service Connectivity Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Express Route Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-expressroute)
* [Learn more about NPM Frequently asked questions](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-faq)
