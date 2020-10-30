<properties
	pageTitle="Troubleshooting login performance"
	description="Troubleshooting login performance"
	infoBubbleText="Troubleshooting login performance"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="6fc4811c-c076-4c15-b286-463ba214b770"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32745062"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
    
# Troubleshooting login performance

Slow login issues can have many different root causes. Work through the recommended steps to solve for the most common issues.

## **Recommended Steps**

* Monitor the resource consumption of your server. If you are maxing out IO, memory or compute resources, scale up the resource that you are limited on.
* If your client is hosted in an Azure VM use accelerated networking for lowest connection latency
* Use connection pooling to avoid the overhead of setting up many short lived connections

## **Recommended Documents**

* [Accelerated networking for Linux VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)
* [Accelerated networking for Windows VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
* [Monitoring with Grafana](https://docs.microsoft.com/azure/azure-arc/data/monitor-grafana-kibana)


