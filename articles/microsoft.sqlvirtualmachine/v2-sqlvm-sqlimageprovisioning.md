<properties
  pagetitle="SQL Image Provisioning&#xD;"
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

If you are planning to deploy a SQL inside a Virtual Machine, follow the [Provision SQL Server using Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision) guide.

## **Recommended Steps**


* **Deploy SQL with a different Locale/Language**

   You cannot change locale at Image provisioning but can follow the steps at [Change the SQL Locale](https://techcommunity.microsoft.com/t5/sql-server-support/change-locale-language-of-sql-server-on-azure-vm/ba-p/1707566) post deployment.
 
* **Changing SQL Collation**
   
  Currently you cannot change the collation for SQL Server if you are provisioning an image from the Azure Marketplace. You need to 
  [Rebuild the system databases to change the Collation](https://docs.microsoft.com/sql/relational-databases/collations/set-or-change-the-server-collation?view=sql-server-ver15) after the image is deployed.

* **Generalize  or SysPrep SQL VM**

  You have two ways to generalize SQL Server on Azure VM:

   * Start with OS only VM and follow regular two-step [SQL Sysprep Process](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15), followed by [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
   * Use one of our SQL VM images and use [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource). If you are following this, make sure you [add SQL login to the generalized VM and you delete the registry key mentioned here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images).

* **SQL BYOL Image Deployment fails**

  You need to have [Enterprise Agreement](https://docs.microsoft.com/azure/cost-management-billing/manage/ea-portal-get-started) and [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?rtc=1&activetab=software-assurance-default-pivot%3aprimaryr3) to deploy SQL Server BYOL Images on Azure. Azure Cloud Solution Partner (CSP) cannot deploy BYOL images. You can deploy Pay-as-you-go images and then [Enable Azure hybrid benefits](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal#vms-already-registered-with-the-resource-provider) to bring their own licenses.

* **Cannot Deploy SQL VM due to Capacity or Quota limits**
 
   Please follow the article to [Increase the limits](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests).

* **I am looking for the SQL Setup Media to change the edition or version of SQL Server or install another instance**

  Customers who have [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?rtc=1&activetab=software-assurance-default-pivot%3aprimaryr3) can obtain their installation media from the [Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx). Customers that do not have software assurance can use the setup media from a Marketplace SQL Server VM image (located at ***C:\SQLServerFull**) that has their desired edition.

* **Changing Default Drive for SQL installation**
  
  If you deploy any SQL Server Marketplace image, then it is not possible to change the installation directory during provisioning. By default, we will install the binaries in C drive. To have SQL binaries/installation on a different drive: <br>

  * Uninstall the SQL and its Shared Features and Reinstall on a different drive
  * Create a Windows only VM and copy the SQL Setup file from the source VM or from Volume licensing and install it on the desired destination VM. Post installation make sure you change the licensing using [SQL Virtual Machine](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/licensing-model-azure-hybrid-benefit-ahb-change?tabs=azure-portal) so that it reflects the correct billing for your VM.

## **Recommended Documents**

* [Install SQL with sysprep](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15)
* [Create Managed Image of Generalized VM](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
* [FAQ on SQL Images](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images)
* [Provisioning SQL VM with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-ps-sql-create)
* [Deploy SQL using Azure quickstart templates](https://azure.microsoft.com/resources/templates/?term=sql)
* [Provision SQL Server from Azure Portal](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-portal-sql-server-provision)