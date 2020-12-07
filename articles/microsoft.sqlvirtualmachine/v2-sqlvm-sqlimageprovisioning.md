<properties
  pagetitle="SQL Image Provisioning"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740092"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="11c09f5c-18a1-40b6-ae41-176dac796d53"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Image Provisioning

This article addresses common questions and issues related to deploying SQL Server inside an Azure Virtual Machine (VM). For deployment instructions, see [Provision SQL Server using Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision).

## **Recommended Steps**


* **Deploy SQL with a different Locale/Language**

   You can only change the locale after image provisioning is completed. See [Change the SQL Locale](https://techcommunity.microsoft.com/t5/sql-server-support/change-locale-language-of-sql-server-on-azure-vm/ba-p/1707566).
 
* **Change the SQL Collation**
   
  Currently you cannot change the collation for SQL Server if you are provisioning an image from the Azure Marketplace. After the image is deployed, you must 
  [rebuild the system databases to change the Collation](https://docs.microsoft.com/sql/relational-databases/collations/set-or-change-the-server-collation?view=sql-server-ver15).

* **Generalize or SysPrep SQL VM**

  You can generalize SQL Server on Azure VM in one of two ways:

   * Start with an OS-only VM, and follow the regular two-step [SQL Sysprep Process](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15). Follow this with [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource).
   * Use one of our SQL VM images and follow [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource). Make sure that you [add the SQL login to the generalized VM and delete the registry key mentioned here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images).
   
* **SQL BYOL Image deployment fails**

   To deploy SQL Server BYOL Images on Azure, you must have the [Enterprise Agreement](https://docs.microsoft.com/azure/cost-management-billing/manage/ea-portal-get-started) and [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?rtc=1&activetab=software-assurance-default-pivot%3aprimaryr3). Azure Cloud Solution Partner (CSP) cannot deploy BYOL images. You can deploy Pay-as-you-go images and then [enable Azure hybrid benefits](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal#vms-already-registered-with-the-resource-provider) to bring their own licenses.

* **Cannot deploy SQL VM due to capacity or quota limits**
 
   To resolve, [increase the limits](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests).

* **I need the SQL Setup Media to change the edition or version of SQL Server or install another instance**

  Customers who have [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?rtc=1&activetab=software-assurance-default-pivot%3aprimaryr3) can obtain their installation media from the [Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx). Customers that do not have Software Assurance can use the setup media from a Marketplace SQL Server VM image (located at **C:\SQLServerFull**) which has their desired edition.

* **Change the default drive for SQL installation**
  
  If you're deploying any SQL Server Marketplace image, you cannot change the installation directory during provisioning. By default, the binaries are installed in the C drive. 
  
  To install SQL binaries/installation on a different drive: <br>

  * Uninstall the SQL and its Shared Features, and reinstall on a different drive
  * Create a Windows-only VM. Copy the SQL Setup file from the source VM or from Volume licensing and install it on the desired destination VM. After installation, make sure that you change the licensing using [SQL Virtual Machine](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal) so that it reflects the correct billing for your VM.

## **Recommended Documents**

* [Install SQL with sysprep](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15)
* [Create Managed Image of Generalized VM](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
* [FAQ on SQL Images](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images)
* [Provisioning SQL VM with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-ps-sql-create)
* [Deploy SQL using Azure quickstart templates](https://azure.microsoft.com/resources/templates/?term=sql)
* [Provision SQL Server from Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision)
