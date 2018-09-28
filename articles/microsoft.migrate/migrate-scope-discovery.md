<properties
	pageTitle="Scope discovery in Azure Migrate"
	description="Issues and guidance regarding how to scope discovery in Azure Migrate"
	service="microsoft.migrate"
	resource="projects"
	authors="nsoneji"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593695"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
/>

# Scope discovery in Azure Migrate

## **Recommended steps**

### **How can I scope discovery for a multi-tenant environment in Azure Migrate?**
Azure Migrate allows you to split the discovery of your VMs to ensure that VMs of one tenant are not discovered in another tenant's subscription. [Learn more](https://docs.microsoft.com/azure/migrate/resources-faq#how-can-i-discover-a-multi-tenant-environment-in-azure-migrate) about how you can split the discovery in Azure Migrate.

### **How can I discover a large environment in Azure Migrate?**
Azure Migrate allows you to discover upto 1500 VMs in a single discovery. To discover a large environment, you can split your discoveries into multiple projects. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-scale-assessment) about how you can discover a large environment. 

### **What data is collected by Azure Migrate?**
Azure Migrate supports two kinds of discovery, appliance-based discovery and agent-based discovery. The appliance-based discovery collects metadata about the on-premises VMs, the complete list of metadata collected by the appliance is listed [here](https://docs.microsoft.com/azure/migrate/resources-faq#what-data-is-collected-by-azure-migrate).
The agent-based discovery is an option available on top of the appliance-based discovery and helps customers [visualize dependencies](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies) of the on-prem VMs. The dependency agents collect details like, FQDN, OS, IP address, MAC address, processes running inside the VM and the incoming/outgoing TCP connections from the VM.
