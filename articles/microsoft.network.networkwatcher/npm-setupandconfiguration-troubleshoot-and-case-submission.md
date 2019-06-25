<properties
	pageTitle="I am unable to see my agent in the Nodes page"
	description="I am unable to see my agent in the Nodes page"
	service="Microsoft.OperationalInsights"
	resource="Microsoft.OperationsManagement/solutions"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32606425"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
/>

# No Agent in Nodes

## **Recommended Steps**

### Unable to see agent in the Nodes page

* Check the Log Analytics workspace id and key entered for the agent during setup. [Use this link for reference]( https://docs.microsoft.com/en-us/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard)<br>
* To check if the agent is up, open a command prompt and run `tasklist |findstr NPMDAgent`. If no agent is found, Microsoft Monitoring Agent it is not running. Start it manually. 

### **No Data in NPM**

 * If you have not [created rules](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor#configure-the-solution), go to "Configure" to create rules, select source and destinations, and set thresholds to start monitoring
 * Based on frequency set in the test, it may take the data about 30 mins to appear in the dashboard
 * To check if NPM is receiving any data, run `NetworkMonitoring | take 5` in Log Analytics for your workspace

## **Recommended Documents**

* [Learn more about NPM agent](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/agent-windows)<br>
* [Learn more about NPM](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Performance Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Express Route Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor-expressroute)
* [Learn more about NPM Frequently asked questions](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor-faq)
