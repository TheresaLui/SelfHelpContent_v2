<properties
	pageTitle="General Licensing questions"
	description="General Licensing questions"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	articleId="deefbfc5-9904-4cad-ad74-d95e0ed297c3"
	selfHelpType="generic"
	supportTopicIds="32740081"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	ownershipId="AzureData_AzureSQLVM"
/>

# General Licensing Questions
**How can I install my licensed copy of SQL Server on an Azure VM?**
<br>There are three ways to do this. If you're an enterprise agreement (EA) customer, you can provision one of the virtual machine images that supports licenses, which is also known as bring-your-own-license (BYOL). If you have software assurance, you can enable the Azure Hybrid Benefit on an existing pay-as-you-go (PAYG) image. Or you can copy the SQL Server installation media to a Windows Server VM, and then install SQL Server on the VM. Be sure to register your SQL Server VM with the resource provider for features such as portal management, automated backup and automated patching.

**Can I change a VM to use my own SQL Server license if it was created from one of the pay-as-you-go gallery images?**
<br>Yes. You can easily switch a pay-as-you-go (PAYG) gallery image to bring-your-own-license (BYOL) by enabling the Azure Hybrid Benefit. For more information, see How to change the licensing model for a SQL Server VM. Currently, this facility is available only for Public Cloud customers.

**Will switching licensing models require any downtime for SQL Server?**
<br>No. Changing the licensing model does not require any downtime for SQL Server as the change is effective immediately and does not require a restart of the VM. However, to register your SQL Server VM with the SQL Server VM resource provider, the SQL IaaS extension is a prerequisite and installing the SQL IaaS extension in full mode restarts the SQL Server service. As such, if the SQL IaaS extension needs to be installed, either install it in lightweight mode for limited functionality, or install it in full mode during a maintenance window. The SQL IaaS extension installed in lightweight mode can be upgraded to full mode at any time, but requires a restart of the SQL Server service.

**Is it possible to switch licensing model on a SQL Server VM deployed using classic model?**
<br>No. Changing licensing model is not supported on a classic VM. You may migrate your VM to the Azure Resource Manager model and register with the SQL Server VM resource provider. Once the VM is registered with the SQL Server VM resource provider, licensing model changes will be available on the VM.

**Can I use the Azure portal to manage multiple instances on the same VM?**
<br>No. Portal management is a feature provided by the SQL Server VM resource provider, which relies on the SQL Server IaaS Agent extension. As such, the same limitations apply to the resource provider as to the extension. The portal can either only manage one default instance, or one named instance, as long as it was configured correctly. For more information on these limitations, see SQL Server IaaS agent extension.

**Can CSP subscriptions activate the Azure Hybrid Benefit?**
<br>Yes, the Azure Hybrid Benefit is available for CSP subscriptions. CSP customers should first deploy a pay-as-you-go image, and then change the licensing model to bring-your-own-license.

**Do I have to pay to license SQL Server on an Azure VM if it is only being used for standby/failover?**
<br>To have a free passive license for a standby secondary availability group or failover clustered instance, you must meet all of the following criteria as outlined by the Product Licensing Terms:

* You have license mobility through Software Assurance
* The passive SQL Server instance does not serve SQL Server data to clients or run active SQL Server workloads. It is only used to synchronize with the primary server and otherwise maintain the passive database in a warm standby state. If it is serving data, such as reports to clients running active SQL Server workloads, or performing any work other than what is specified in the product terms, it must be a paid licensed SQL Server instance. The following activity is permitted on the secondary instance: database consistency checks or CheckDB, full backups, transaction log backups, and monitoring resource usage data. You may also run the primary and corresponding disaster recovery instance simultaneously for brief periods of disaster recovery testing every 90 days.
* The active SQL Server license is covered by Software Assurance and allows for one passive secondary SQL Server instance, with up to the same amount of compute as the licensed active server, only
* The secondary SQL Server VM utilizes the Disaster Recovery license in the Azure portal

**What is considered a passive instance?**
<br>The passive SQL Server instance does not serve SQL Server data to clients or run active SQL Server workloads. It is only used to synchronize with the primary server and otherwise maintain the passive database in a warm standby state. If it is serving data, such as reports to clients running active SQL Server workloads, or performing any work other than what is specified in the product terms, it must be a paid licensed SQL Server instance. 
<br>The following activity is permitted on the secondary instance: database consistency checks or CheckDB, full backups, transaction log backups, and monitoring resource usage data. You may also run the primary and corresponding disaster recovery instance simultaneously for brief periods of disaster recovery testing every 90 days.

**What scenarios can utilize the Disaster Recovery (DR) benefit?**
<br>The licensing guide provides scenarios in which the Disaster Recovery Benefit can be utilized. Refer to your Product Terms and talk to your licensing contacts or account manager for more information.

**Which subscriptions support the Disaster Recovery (DR) benefit?**
<br>Comprehensive programs that offer Software Assurance equivalent subscription rights as a fixed benefit support the DR benefit. This includes. but is not limited to, the Open Value (OV), Open Value Subscription (OVS), Enterprise Agreement (EA), Enterprise Subscription Agreement (EAS), and the Server and Cloud Enrollment (SCE). Refer to the product terms and talk to your licensing contacts or account manager for more information.

**Will registering my VM with the new SQL VM resource provider bring additional costs?**

No. The SQL VM resource provider just enables additional manageability for SQL Server on Azure VM with no additional charges.

**Is the SQL VM resource provider available for all customers?**

Yes. All customers are able to register with the new SQL VM resource provider. However, only customers with Software Assurance Benefit can activate the Azure Hybrid Benefit (AHB) (or BYOL) on a SQL Server VM.

**Where can I find the license key to use for installing SSRS or SSAS 2017+ in an Azure VM?**

If you already have a SQL Server VM with Standard or Enterprise edition created from Azure Marketplace, you can launch setup.exe from ***C:\SQLServerFull***, copy the product key that appears in the install process and exit the installer. You can then apply the key during SSRS or SSAS installation. 

**How can I determine the license type of my SqlVirtualMachine resources?**

You can use the following Powershell command: `(Get-AzureRmResource -ResourceName <vm_name> -ResourceGroupName <resource_group> -ResourceType 'Microsoft.SqlVirtualMachine/SqlVirtualMachines').Properties | Format-List;`

##  **Recommended Documents**

* [Frequently asked questions for SQL Server running on Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq)
* [Pricing guidance for Azure SQL Server VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-pricing-guidance)
