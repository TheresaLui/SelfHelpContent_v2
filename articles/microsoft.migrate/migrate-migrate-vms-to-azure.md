<properties
	pageTitle="Azure Migrate Preview - Migrate VMs to Azure"
	description="Azure Migrate Preview - Migrate VMs to Azure"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631939"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="5ba2cff9-3754-4343-ab0f-ee3b617a32a6"
/>

# Azure Migrate Preview - Migrate VMs to Azure

## **Recommended Steps**

* **Are there any reporting options available to track the migrated VMs? [Basic migration lifecycle tracking of a VM]**

	Yes, within the tool there is an overview page that gives you this information.

* **Is there a option to group the migration VMs during replication and cutover for tracking? [Comes in handy when more than 50 VMs are involved in migration]**

	Currently we are recommending that migrations be performed in batches of 50VMs (that is, not have more than 50 VMs simultaneously replicating at any time). We will be increasing this limit in GA and will add appliance scale-out options after GA to increase simultaneous replication scale. For replication and migration, portal lets you multi-select VMs on which the action is to be performed.
