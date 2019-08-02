<properties
	pageTitle="I installed Traffic Analytics but now face configuration and setup issues"
	description="I installed Traffic Analytics but now face configuration and setup issues"
	service="microsoft.network"
	resource="networkwatchers"
	ms.author="vinigam"
	authors="vinynigam"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32606428"
	resourceTags=""
	productPesIds="16160"
    articleId="ta-config-and-setup"
	cloudEnvironments="public,fairfax,mooncake"
/>

# Traffic Analytics - Configuration and Setup

## **Recommended Steps**

### **Prerequisites to follow before configuring Traffic Analytics**

* Ensure you have the correct user access setup for your account and network watcher enabled for your subscription. [Use this link for reference.](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#prerequisites)<br>

### **Step-by-step Enable Traffic Analytics using Azure Portal**

*  [Use this link for reference](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#enable-flow-log-settings)<br>

### **Bytes and Packets data**

*  To view bytes and packets data in Traffic Analytics, enable Flow Logs version 2. [Use this link for reference]( https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal)<br>

### **Faster procsessing interval**

*  To view bytes and packets data in Traffic Analytics, enable Flow Logs version 2. [Use this link for reference]( https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard)<br>

### **Regions where NSGs can be enabled with Traffic Analytics**

*  Supported regions for NSGs can be found in the official documentation. NSGs in regions other than the supported list cannot be enabled with Traffic Analytics. [Use this link for reference](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#supported-regions)<br>

### **Regions where Log Analytics workspace needs to be created for Traffic Analytics**

*  Regions in which NSG may be enabled with Traffic Analytics and the region in which the Log Analytics workspace collecting data from Traffic Analytics can be different. Regions in which Traffic Analytics supports Log analytics workspaces can be found in official documentation. If region in which Traffic Analytics enabled NSG is present , differs from the region in which workspace resides, you may incur egress costs. [Use this link for reference.](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#supported-regions)<br>

## **Recommended Documents**

* [Learn more about Traffic Analytics solution](https://docs.microsoft.com/azure/network-watcher/traffic-analytics)<br>
* [Learn more about Traffic Analytics schema](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about Traffic Analytics Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
