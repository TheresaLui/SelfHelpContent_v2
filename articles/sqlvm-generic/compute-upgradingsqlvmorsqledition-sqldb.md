<properties
	pageTitle="setup and configuration/upgrading sql vm or sql edition"
	description="setup and configuration/upgrading sql vm or sql edition"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32511160"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public"
/>

# setup and configuration/upgrading sql vm or sql edition

## **Recommended steps**
1. Upgrading to new version or edition: Currently, there is no in-place upgrade for SQL Server running in an Azure VM. Create a new Azure virtual machine with the desired SQL Server version/edition, and then migrate your databases to the new server using standard data migration techniques.<br>
[Migrate a SQL Server database to SQL Server in an Azure VM](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-migrate-sql/)
2. Applying updates and service packs: Virtual machines give you control over the host machine, including when and how you apply updates. For the operating system, you can manually apply windows updates, or you can enable a scheduling service called Automated Patching. Automated Patching installs any updates that are marked important, including SQL Server updates in that category. Other optional updates to SQL Server must be installed manually.<br>
[Automated Patching for SQL Server in Azure Virtual Machines (Resource Manager)](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-automated-patching/)

## **Recommended documents**
[SQL Server on Azure Virtual Machines FAQ](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-sql-server-iaas-faq/?rnd=1)
