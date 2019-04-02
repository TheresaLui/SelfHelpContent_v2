<properties
	pageTitle="Group creation and updates"
	description="Group creation and updates"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32593693"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId=""
/>

# Dependency visualization in Azure Migrate

## **Recommended Steps**

### **How can I automate installation of Microsoft Monitoring Agent (MMA) and dependency agent?**
You can use [script for dependency](https://docs.microsoft.com/azure/monitoring/monitoring-service-map-configure#installation-script-examples) and [script for MMA](https://gallery.technet.microsoft.com/scriptcenter/Install-OMS-Agent-with-2c9c99ab). In addition to scripts, you can also leverage deployment tools like System Center Configuration Manager (SCCM) and [Intigua](https://www.intigua.com/getting-started-intigua-for-azure-migration) to deploy the agents.

### **Is dependency visualization supported for groups with more than 10 VMs?**
You can visualize dependencies of groups with up to 10 VMs, if you have a group with more than 10 VMs, we recommend you to split the group in to smaller groups and visualize dependencies.
