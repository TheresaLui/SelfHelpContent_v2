<properties
	pageTitle="I installed NPM and setup monitoring but topology does not show all the hops"
	description="I installed NPM and setup monitoring but topology does not show all the hops"
	service="microsoft.operationalinsights"
	resource="operationalinsightsaccounts"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds="32626098"
	resourceTags=""
	productPesIds="15725"
	cloudEnvironments="public,fairfax"
/>

# All hops do not show up in topology 

## **Recommended steps**
*  NPM uses traceroute to determine hops in a network and shows them in the topology <br>
Run tracert from the machine hosting the agent with admin permissions and check the hops . These hops should match the hops shown by NPM in the topology


## **Recommended documents**
[Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
