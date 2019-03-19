<properties
	pageTitle="Dependency visualization in Azure Migrate"
	description="Issues and guidance regarding dependency visualization in Azure Migrate"
	service="microsoft.migrate"
	resource="projects"
	authors="shijoy"
	ms.author="shijojoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631899,32631900,32631902"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="3b90d80e-a991-4984-8f86-ddcd06a9a551"
/>

# Dependency visualization in Azure Migrate

## **Recommended Steps**

### **How do I configure Azure Migrate project to use an existing OMS workspace?**
When you configure your OMS workspace for the first time for an Azure Migrate project, you can either create new or use existing OMS workspace. [Learn more](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies#associate-a-log-analytics-workspace) about how to configure OMS workspace.

### **Can I change existing project to use a different OMS workspace?**
No, you cannot change the OMS workspace once it is configured.

### **How can I automate installation of Microsoft Monitoring Agent (MMA) and dependency agent?**
You can use [script for dependency](https://docs.microsoft.com/azure/monitoring/monitoring-service-map-configure#installation-script-examples) and [script for MMA](https://gallery.technet.microsoft.com/scriptcenter/Install-OMS-Agent-with-2c9c99ab). In addition to scripts, you can also leverage deployment tools like System Center Configuration Manager (SCCM) and [Intigua](https://www.intigua.com/getting-started-intigua-for-azure-migration) to deploy the agents.

### **Can I export the dependency visualization report?**
No, currently you cannot export the dependency visualization report. 

### **Can I visualize dependencies for more than one-hour duration?**
No, Azure Migrate lets you visualize dependencies for up to one-hour duration. You can go back to any specific date in the last one month, but the duration for which you can visualize the dependencies is up to 1 hour.

### **Is dependency visualization supported for groups with more than 10 VMs?**
You can visualize dependencies of groups with up to 10 VMs, if you have a group with more than 10 VMs, we recommend you to split the group in to smaller groups and visualize dependencies.

### **I installed agents in my on-prem VMs, but the dependencies are not showing up.**
Typically, the dependencies start showing up after 15-20 minutes of installing the agents. Learn more about [agent installation](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies#download-and-install-the-vm-agents). 

### **What is the supported OS matrix for the Microsoft Monitoring Agent (MMA) and dependency agent?**
Refer to the support matrix document [MMA agent](https://docs.microsoft.com/azure/log-analytics/log-analytics-concept-hybrid#supported-windows-operating-systems) and [dependency agent](https://docs.microsoft.com/azure/monitoring/monitoring-service-map-configure#supported-windows-operating-systems) for details.

### **Can I export the dependency visualization report?**
No, the dependency visualization cannot be exported. However, since Azure Migrate uses Service Map for dependency visualization, you can use the [Service Map REST APIs](https://docs.microsoft.com/rest/api/servicemap/machines/listconnections) to get the dependencies in a JSON format.

