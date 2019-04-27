<properties
	pageTitle="My topology does not show any issue even though NPM shows path as unhealthy "
	description="My topology does not show any issue even though NPM shows path as unhealthy "
	service="Microsoft.Network"
	resource="networkWatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32606422"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
/>

# Topology does not show any issue even though NPM shows path as unhealthy 

## **Recommended steps**
* Health and topology checks are repeated at different frequencies. Traceroute is calculated every 10 mins , whereas health status is updated every 3 mins for Performance Monitor and Express Route Monitor and at custom time set for  Service Connectivity Monitor. Hence there will be a differrence in the topology and health status. To know the closest topology state, use Log Analytics fields TimeProcessed field for health and TracerouteCompletedTime for topology.

## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
