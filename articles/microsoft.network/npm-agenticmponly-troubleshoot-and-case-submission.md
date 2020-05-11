<properties
	pageTitle="My node shows supported protocol as ICMP only"
	description="My node shows supported protocol as ICMP only"
	service="microsoft.network"
	resource="networkwatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32606425"
	resourceTags=""
	productPesIds="16160"
    articleId="npm-agenticmponly-troubleshoot-and-case-submission"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="CloudNet_NetAnalytics"
/>

# Node shows supported protocol as ICMP only in the Nodes page

## **Recommended Steps**

* For Windows Server machines, run EnableRules.ps1 with admin permissions from your now. [Use this link for download EnableRules.ps1](https://gallery.technet.microsoft.com/OMS-Network-Performance-7ec93b2f)<br>
* Check if machine hosting the agent is a Windows client machine. Windows client machines do not support TCP. 

## **Recommended Documents**

* [Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
* [Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
* [Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
