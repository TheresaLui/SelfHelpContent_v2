<properties
	pageTitle="Common issues for Network Watcher Topology"
	description="Common issues for Network Watcher Topology"
	service="microsoft.network"
	resource="networkwatcher"
	authors="damendo"
	ms.author="damendo"
	displayOrder="2"
	articleId="a49b4a9b-4a4d-e3ce-744d-4982e821db9c"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32583552"
	resourceTags=""
	productPesIds="16160"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_NetAnalytics"
/>


# Network Watcher Topology Common issues

The Topology view in Network Watcher shows you the resources in your virtual network and the relationships between them.

## **Recommended Steps**

* Read the [Topology overview](https://docs.microsoft.com/azure/network-watcher/view-network-topology)

### **I can't see all my resources in the Topology view**

Topology view only works at the **resource group** and **virtual network** levels. Virtual Machines and other resources which are in different resource groups (or subscriptions) will not show up, even if they are connected to resources in the current resource group.

### **I get a "User does not have permission to perform topology action" error**

Request permission from the owner of your subscription. You need to have the [networkWatcher/Topology permission](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions#topology). This is not available with the current "Reader" role and you may have to create a custom role in case you do not want to provide "Contributor" or higher access.
