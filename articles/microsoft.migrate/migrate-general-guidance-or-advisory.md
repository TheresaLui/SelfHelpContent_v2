<properties
	pageTitle="Azure Migrate service"
	description="Advisory guidance for Azure Migrate"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32613311,32593684,32631908,32632323,32631909"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="547f6735-a09e-46e9-bfb4-d59bbecb1284"
/>

# Azure Migrate Service 

## **Recommended Steps**

* **Can I migrate on-premises VMs to Azure using Azure Migrate service?**

	No, Azure Migrate does not migrate VMs, it is only used for **planning** migration of on-premises VMs to Azure. Once planning is done, you can use [Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/site-recovery-overview) service to migrate the VMs to Azure.

* **Is your issue or query related to the [Azure Migrate](https://azure.microsoft.com/services/azure-migrate) Service?**

	Use 'Migrate' service only if your issue or query is related to the Azure Migrate service such as issues related to Azure Migrate discovery, assessment or dependency visualization. If you are not using Azure Migrate, use the respective service to find solution or raise a support ticket. 

* **Migrate from ASM to ARM**

	Based on resources to be migrated to ARM use the corresponding service. For example, if you are migrating a Linux VM from ASM to ARM, file a support ticket on 'Virtual Machines running Linux' 

* **Any issue in a VM migration using Azure Site Recovery**

	Use 'Site Recovery' Service.

* **Migrate an application to Azure as a PaaS service**

	Use corresponding PaaS service. For example, if you are migrating an Active Directory, use 'Azure Active Directory' service.

* **Migrate resources from one subscription to other subscription**

	Use the corresponding service for the resource being migrated. For example, to migrate Azure VMs (Windows) from one subscription to another subscription, use 'Virtual Machine running Windows" service.

* **Migrate databases to Azure**

	Use 'Database Migration Service' service.

* **Migrate Managed disks to Unmanaged disks or Unmanaged disks to Managed disks in Azure**

	Use 'Storage Account Management' service.

* **Migrate Managed disk to different subscription**

	Use 'Storage Account Management' service.
