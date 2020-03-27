<properties
	pageTitle="I am unable to see my agent in the Nodes page"
	description="I am unable to see my agent in the Nodes page"
	service="microsoft.network"
	resource="networkWatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32606425"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="MoonCake"
	articleId="npm-setupandconfiguration-troubleshoot-and-case-submission-mooncake"
	ownershipId="CloudNet_NetAnalytics"
/>

# Agent Setup and Configuration issues

## **Recommended Steps**

### Unable to see agent in the Nodes page

* [Check the Log Analytics workspace id](https://docs.azure.cn/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard) and key entered for the agent during setup
* Check if the agent is up and running. Open a CMD prompt and run `tasklist |findstr NPMDAgent`. If agent is not found, that means it is not running. Look for **Microsoft Monitoring Agent** and start it.

### **No Data in NPM**

 * If you have not [created rules](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor#configure-the-solution), go to "Configure" to create rules, select source and destinations, and set thresholds to start monitoring
 * Based on frequency set in the test, it may take the data about 30 mins to appear in the dashboard
 * To check if NPM is receiving any data, run `NetworkMonitoring | take 5` in Log Analytics for your workspace

## **Recommended Documents**

* [Learn more about NPM agent](https://docs.azure.cn/azure-monitor/platform/agent-windows)
* [Learn more about NPM](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Performance Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Service Connectivity Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor)
* [Learn more about NPM Express Route Monitor](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-expressroute)
* [Learn more about NPM Frequently asked questions](https://docs.azure.cn/azure-monitor/insights/network-performance-monitor-faq)
