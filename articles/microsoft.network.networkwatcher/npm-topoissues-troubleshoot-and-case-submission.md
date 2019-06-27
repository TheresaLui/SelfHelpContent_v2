<properties
	pageTitle="I installed NPM and setup monitoring but topology does not show all the hops"
	description="I installed NPM and setup monitoring but topology does not show all the hops"
	service="microsoft.network"
	resource="networkWatchers"
	authoralias="vinigam"
	authors="vinynigam"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds="32642176"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
	articleId="npm-topoissues-troubleshoot-and-case-submission"
/>

# Topology Issues

## **Recommended steps**
* NPM uses traceroute to determine hops in a network and shows them in the topology <br>
Run traceroute from the machine hosting the agent with admin permissions and check the hops . These hops should match the hops shown by NPM in the topology. Routers need to be accessible by traceroute. For on-premise hops/network devices , ensure ICMP_TTL_EXCEEDED is enabled. Azure does not expose its hops to traceroute, hence they will continue to show up as undefined.<br>

* Health and topology checks are repeated at different frequencies. Traceroute is calculated every 10 mins , whereas health status is updated every 3 mins for Performance Monitor and Express Route Monitor and at custom time set for Service Connectivity Monitor. Hence there will be a difference in the topology and health status. To know the closest topology state, use Log Analytics fields TimeProcessed field for health and TracerouteCompletedTime for topology.


## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute) <br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
