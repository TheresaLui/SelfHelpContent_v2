<properties
  pagetitle="SQL Server Setup or Patching"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740100"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="08d70dfd-4a85-4c6a-b47f-177c66a6f806"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Server Setup or Patching

If you have issues with SQL or its patching, you will need to check [Setup Bootstrap logs](https://docs.microsoft.com/sql/database-engine/install-windows/view-and-read-sql-server-setup-log-files?view=sql-server-ver15) or upload for Microsoft's analysis.

## **Recommended Steps**

* **Deploy SQL with a different Locale/Language**

   You cannot change locale at Image provisioning but can follow the steps at [Change the SQL Locale](https://techcommunity.microsoft.com/t5/sql-server-support/change-locale-language-of-sql-server-on-azure-vm/ba-p/1707566) post deployment.
 
* **Changing SQL Collation**
   
  Currently you cannot change the collation for SQL Server if you are provisioning an image from the Azure Marketplace. You need to 
  [Rebuild the system databases to change the Collation](https://docs.microsoft.com/sql/relational-databases/collations/set-or-change-the-server-collation?view=sql-server-ver15)  after the image is deployed.

* **Can I install a second instance of SQL Server on the same VM? Where can I find the SQL installation Setup file?**

    Yes. The SQL Server installation media is located at **C:\SQLServerFull** path. Run Setup.exe from that location to add new SQL Server instances or to change other installed features of SQL Server on the machine. Customers who have [Software Assurance](https://www.microsoft.com/licensing/licensing-programs/software-assurance-default?rtc=1&activetab=software-assurance-default-pivot%3aprimaryr3) can obtain their installation media from the [Volume Licensing Center](https://www.microsoft.com/Licensing/servicecenter/default.aspx). Customers that do not have software assurance can use the setup media from a Marketplace SQL Server VM image that has their desired edition.

* **Generalize or SysPrep SQL VM**

  You have two ways to generalize SQL Server on Azure VM:

   * Start with OS only VM and follow regular two-step [SQL Sysprep Process](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?view=sql-server-ver15), followed by [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
   * Use one of our SQL VM images and use [Windows Sysprep](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource). If you are following this, make sure you [add SQL login to the generalized VM and you delete the registry key mentioned here](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#images)

* **How do I change to a different version or edition of the SQL Server in an Azure VM?**
   * To **upgrade or downgrade SQL Version**, please follow  [In-place Change of SQL Server Version on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-version)
   * To **upgrade or downgrade SQL Edition**, please follow  [In-place Change of SQL Server Edition on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/change-sql-server-edition)

* **How are updates and service packs applied on a SQL Server VM?**

  For the operating system, you can manually apply windows updates, or you can enable a scheduling service called [Automated Patching](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-patching). Automated Patching installs any updates that are marked important, including SQL Server updates in that category. Other optional updates to SQL Server must be installed manually.
  
* **How can I get free extended security updates for my end of support SQL Server 2008 and SQL Server 2008 R2 instances?**

  You can get [Free Extended security updates](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-2008-eos-extend-support) by moving your SQL Server as-is to an Azure SQL virtual machine. For more information, see [End of support options](https://docs.microsoft.com/sql/sql-server/end-of-support/sql-server-end-of-life-overview?view=sql-server-ver15).

* **Can I remove SQL Server completely from a SQL Server VM?**

    Yes, but you will continue to be charged for your SQL Server VM as described in [Pricing guidance](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-pricing-guidance). If you no longer need SQL, you can deploy a new Windows VM and migrate the data and applications to the new VM.

## **Recommended Documents**

* [Setup and Patching FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-faq#updating-and-patching)
* [Change SQL Edition](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-change-edition)
* [Automated Patching Feature](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-automated-patching)
* [Information on installing updates](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-servicing-updates?view=sql-server-ver15)
