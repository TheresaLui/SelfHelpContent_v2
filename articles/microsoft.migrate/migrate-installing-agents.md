<properties
	pageTitle="Dependency visualization in Azure Migrate - Installing agents"
	description="Issues and guidance regarding dependency visualization in Azure Migrate - Installing agents"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631900"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="3b90d80e-a991-4984-8f86-ddcd06a9a551"
/>

# Dependency visualization in Azure Migrate - Installing agents

## **Recommended Steps**

* **How can I automate installation of Microsoft Monitoring Agent (MMA) and dependency agent?**

	You can use [script for dependency](https://docs.microsoft.com/azure/monitoring/monitoring-service-map-configure#installation-script-examples) and [script for MMA](https://gallery.technet.microsoft.com/scriptcenter/Install-OMS-Agent-with-2c9c99ab). In addition to scripts, you can also leverage deployment tools like System Center Configuration Manager (SCCM) and [Intigua](https://www.intigua.com/getting-started-intigua-for-azure-migration) to deploy the agents.

* **I installed agents in my on-prem VMs, but the dependencies are not showing up.**

	Typically, the dependencies start showing up after 15-20 minutes of installing the agents. Learn more about [agent installation](https://docs.microsoft.com/azure/migrate/how-to-create-group-machine-dependencies#download-and-install-the-vm-agents). 
