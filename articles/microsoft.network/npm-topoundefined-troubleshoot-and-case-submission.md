<properties
	pageTitle="I installed NPM and setup monitoring but topology shows all hops as undefined"
	description="I installed NPM and setup monitoring but topology shows all hops as undefined"
	service="microsoft.network"
	resource="networkwatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32606422"
	resourceTags=""
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
/>

# All hops in topology show up as undefined

## **Recommended steps**
*  Routers need to be accessible by traceroute. For on-premise hops/network devices , ensure ICMP_TTL_EXCEEDED is enabled <br>
*  Azure does not expose its hops to traceroute, hence they will continue to show up as undefined


## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
