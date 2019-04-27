<properties
	pageTitle="I installed NPM and setup monitoring in Service Connectivity Monitor but I do not see any data in the dashboard"
	description="I installed NPM and setup rules  but I do not see any data for my rule"
	service="Microsoft.Network"
	resource="networkWatchers"
	ms.authoralias="vinigam"
	authors="vinynigam"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32606443"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
/>

# No monitoring data in NPM for a specific rule 

## **Recommended steps**
*  To check if NPM is receiving any data for a specific test, run the below mentioned query in LogAnalytics for your workspace <br>  
```
NetworkMonitoring
| where TestName == "<<Your Service Connectivity Monitor test name>>"
| take 5
* It takes NPM about 30 mins to start showing data after initial setup
```

## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
