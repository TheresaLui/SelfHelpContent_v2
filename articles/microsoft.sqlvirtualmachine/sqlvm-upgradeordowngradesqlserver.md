<properties
	pageTitle="sql administration/upgrade or downgrade SQL"
	description="sql administration/upgrade or downgrade SQL"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	ms.author="yareyes"
	displayOrder=""
	articleId="d2598f27-28fd-42ac-9375-280df1d0933f"
	selfHelpType="generic"
	supportTopicIds="32633525"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="public"
/>

# sql administration/upgrade or downgrade SQL

* **How can I change the edition of the SQL Server in an Azure VM?**

	The per hour price rate associated with the SQL VM is defined by the edition of SQL Server. Today, we do not offer a mechanism to update the per hour price rate of the VM when SQL Server edition is updated, therefore, we do not support SQL Server edition upgrade or downgrade on an Azure VM. A new VM from the image with the required SQL Server edition should be created to reflect the pricing differences accurately.

* **How do I upgrade SQL Server version in an Azure VM?**

	Free SQL server version upgrades is only available for customers with [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?activetab=software-assurance-default-pivot%3aprimaryr3). If you have SA benefit, you can use [VLSC portal](https://www.microsoft.com/Licensing/servicecenter/default.aspx) to access SQL server installation media and manually upgrade SQL Server version on the VM.

* **How do I downgrade SQL Server version in an Azure VM?**

	You cannot downgrade SQL Server version on the VM. Create a new Azure virtual machine with the desired SQL Server edition, and then migrate your databases to the new server using [standard data migration techniques](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-migrate-sql/).

* **Can I remove SQL Server completely from a SQL VM?**

	You can uninstall SQL Server on Azure VM by using the installation media located on the VM OS drive. but this will not remove any SQL Server license related charges associated with the VM. If you do not need the SQL VM you should stop/deallocate the VM to stop any further charges occur.

##  **Recommended Documents**

* [Frequently asked questions for SQL Server running on Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq)
