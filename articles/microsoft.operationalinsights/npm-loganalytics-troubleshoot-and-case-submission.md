<properties
	pageTitle="I installed NPM and setup monitoring but face issues"
	description="I installed NPM and setup monitoring but face issues"
	service="microsoft.operationalinsights"
	resource="operationalinsightsaccounts"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32626098"
	resourceTags=""
	productPesIds="15725"
	articleId= "npm-loganalytics-troubleshoot-and-case-submission-opin"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Network monitoring (NPM)

## **Recommended Steps**

### **Agent Issues**

*  Agent not visible in Nodes page - Check the Log Analytics workspace id and key entered for the agent during setup. [Use this link for reference]( https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard)<br>

*  Agent not visible in Nodes page - Check if the agent is up and running by following this step<br>
Go to CMD prompt and run the command below. If agent is not found, that means it is not running. Look for Microsoft Monitoring Agent and start it. 

```
tasklist |findstr NPMDAgent .
```

### **No Data in NPM**

* If you have not created rules, go to "Configure" to create rules , select source and destinations and set thresholds to start monitoring. [Learn more](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor#configure-the-solution)<br>

* Based on frequency set in the test, it take data about 30 mins to appear in the dashboard 

* To check if NPM is receiving any data, run the below mentioned query in Log Analytics for your workspace: <br> 

```
NetworkMonitoring | take 5
```

* To check if Performance Monitor tests are recording data, run the below mentioned query in Log Analytics for your workspace: <br> 

``` 
NetworkMonitoring | where SubType == "SubNetwork" | where SourceSubNetwork == "<<Your SubNetworkNetwork IP>>"
```

* To check if Performance Monitor is receiving any data for a given network, run the below mentioned query in Log Analytics for your workspace: <br> 

``` 
NetworkMonitoring
| where SubType == "Network"
| where SourceNetwork == "<<Your Network name>>"
```

* To check if Service Connectivity Monitor tests are recording data, run the below mentioned query in Log Analytics for your workspace: <br> 

```
NetworkMonitoring
| where TestName == "<<Your Service Connectivity Monitor test name>>"
| take 5
```

* To check if Express Route Monitor circuits are recording data, run the below mentioned query in Log Analytics for your workspace: <br> 

```
NetworkMonitoring 
| where SubType == "ExpressRouteCircuitUtilization" 
| project CircuitName
```

* To check if Express Route Monitor peerings are recording data, run the below mentioned query in Log Analytics for your workspace: <br>  

```
NetworkMonitoring 
| where SubType == "ExpressRoutePeeringUtilization"
| project CircuitName,PeeringName
```

* Check circuit and peering metrics in Azure Monitor to see if circuit and peering are receiving any data.If there is no data in ExpressRoute Monitor and in Azure monitor, reach out to Express Route team[Learn more](https://docs.microsoft.com/azure/expressroute/expressroute-monitoring-metrics-alerts)<br>

### **Topology Issues**

*  NPM uses traceroute to determine hops in a network and shows them in the topology <br>
Run tracert from the machine hosting the agent with admin permissions and check the hops . These hops should match the hops shown by NPM in the topology. Routers need to be accessible by traceroute. For on-premise hops/network devices , ensure ICMP_TTL_EXCEEDED is enabled.Azure does not expose its hops to traceroute, hence they will continue to show up as undefined.<br> 

* Health and topology checks are repeated at different frequencies. Traceroute is calculated every 10 mins , whereas health status is updated every 3 mins for Performance Monitor and Express Route Monitor and at custom time set for  Service Connectivity Monitor. Hence there will be a difference in the topology and health status. To know the closest topology state, use Log Analytics fields TimeProcessed field for health and TracerouteCompletedTime for topology.

## **Recommended Documents**

* [Learn more about NPM agent](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)<br>
* [Learn more about NPM](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Performance Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Service Connectivity Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about NPM Express Route Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-expressroute)<br>
* [Learn more about NPM Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)