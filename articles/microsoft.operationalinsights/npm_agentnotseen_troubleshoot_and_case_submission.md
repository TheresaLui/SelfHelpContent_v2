<properties
	pageTitle="I am unable to see my agent in the Nodes page"
	description="I am unable to see my agent in the Nodes page"
	service="Microsoft.OperationalInsights"
	resource="Microsoft.OperationsManagement/solutions"
	authoralias="vinigam"
	authors="vinynigam"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32606425"
	resourceTags="optional"
	productPesIds="16160"
	cloudEnvironments="public,fairfax"
/>

# Unable to see  agent in the Nodes page

## **Recommended steps**
* Check the Log Anlaytics worksapce id and key entered for the agent during setup. [Use this link for reference]( https://docs.microsoft.com/en-us/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard)<br>
* Check if the agent is up and running by following this step<br>
Go to CMD prompt and run the command below.
```
tasklist |findstr NPMDAgent .
```
 If agent is not found, that means it is not running. Look for Microsoft Monitoring Agent and start it. 


## **Recommended documents**
[[Learn more about NPM agent](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/agent-windows)<br>
[Learn more about NPM](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Performance Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor)<br>
[Learn more about NPM Express Route Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor-expressroute<br>
[Learn more about NPM Frequently asked questions](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/network-performance-monitor-faq)
