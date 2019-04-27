<properties
	pageTitle="I installed NPM and setup monitoring in Performance Monitor but I do not see any data in the dashboard"
	description="I installed NPM and setup monitoring in Performance Monitor  but I do not see any data in the dashboard"
	service="Microsoft.OperationalInsights"
	resource="Microsoft.OperationsManagement/solutions"
	authoralias="vinigam"
	authors="vinynigam"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32606442"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
/>

# No monitoring data in NPM for a specific network in Performance Monitor 

## **Recommended steps**
*  To check if NPM is receiving any data for a given network, run the below mentioned query in LogAnlaytics for your workspace <br> 
``` 
NetworkMonitoring
| where SubType == "Network"
| where SourceNetwork == "<<Your Network name>>"
```
*  To check if NPM is receiving any data for a given subnetwork, run the below mentioned query in LogAnlaytics for your workspace <br>  
```
NetworkMonitoring
| where SubType == "SubNetwork"
| where SourceSubNetwork == "<<Your SubNetworkNetwork IP>>"
```
*  To check if NPM is receiving any data for a given rule, run the below mentioned query in LogAnlaytics for your workspace <br>  
```
NetworkMonitoring
| where RuleName == "<<Your rule name>>"
```
* It takes NPM about 30 mins to start showing data after initial setup


## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor-expressroute<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor-faq)
