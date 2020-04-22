<properties
pageTitle="trafficanalytics/configandsetup"
description="trafficanalytics/configandsetup"
	service="microsoft.network"
	resource="networkwatcher"
	authors="damendo"
    	ms.author="damendo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32606428"
	resourceTags=""
	productPesIds="16160"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="e3b833f6-76e6-4404-9a32-47671b5d5016"
	ownershipId="CloudNet_NetAnalytics"
/>

# Traffic Analytics - Configuration and Setup

## **Recommended Steps**

### **Prerequisites to follow before configuring Traffic Analytics**

* Ensure you have the [correct user access setup for your account, and network watcher enabled for your subscription](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#prerequisites)
* [Enable Traffic Analytics using Azure Portal](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#enable-flow-log-settings)<br>

### **Bytes and Packets data**

*  To view bytes and packets data in Traffic Analytics, [enable Flow Logs version 2]( https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal)<br>

### **Faster processing interval**

*  To [view bytes and packets data in Traffic Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#install-the-agent-using-setup-wizard), enable Flow Logs version 2

### **Regions where NSGs can be enabled with Traffic Analytics**

*  Supported regions for NSGs can be found in the [documentation](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#supported-regions). NSGs in regions other than the supported list cannot be enabled with Traffic Analytics.

### **Regions where Log Analytics workspace needs to be created for Traffic Analytics**

*  Regions in which NSG may be enabled with Traffic Analytics and the region in which the Log Analytics workspace collecting data from Traffic Analytics can be different. Regions in which Traffic Analytics supports Log analytics workspaces can be found in [documentation](https://docs.microsoft.com/azure/network-watcher/traffic-analytics#supported-regions). If region in which Traffic Analytics enabled NSG is present differs from the region in which workspace resides, you may incur egress costs. 

## **Recommended Documents**

* [Learn more about Traffic Analytics solution](https://docs.microsoft.com/azure/network-watcher/traffic-analytics)<br>
* [Learn more about Traffic Analytics schema](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor)<br>
* [Learn more about Traffic Analytics Frequently asked questions](https://docs.microsoft.com/azure/azure-monitor/insights/network-performance-monitor-faq)
