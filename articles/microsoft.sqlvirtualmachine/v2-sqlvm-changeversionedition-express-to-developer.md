<properties
  pagetitle="Change SQL Server Edition on Azure VM from Express to Developer"
  description="Change SQL Server Edition on Azure VM from Express to Developer"
  infoBubbleText="Change SQL Server Edition on Azure VM from Express to Developer"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="amamun,ujpat"
  selfhelptype="diagnostics"
  supporttopicids="32740074"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="388dd5b7-91e0-4e7b-af70-0464884b0bf7-expresstodeveloper"
  ownershipid="AzureData_AzureSQLVM" />

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
You can upgrade your express edition to developer edition with the steps listed below 
<!--/issueDescription-->

## **Recommended Steps**

1. Take the VM SnapShot backup, and also perform a database backup
2. Provision a VM from Azure Marketplace with SQL 2017 Developer Edition. Alternatively, you can download the Developer Edition from the [Microsoft Download Center](https://www.microsoft.com/en-US/download).
3. Copy the setup file from the path (C:SqlServerFull) to the SQL 2017 Express edition
4. Go to **Maintenance** > **Edition Upgrade**
![EditionUpgrade.png](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/media/change-sql-server-edition/edition-upgrade.png) 
5.  From Azure portal, under **Settings** > **Configure**, change the **Edition** to **Developer**
![PortalDeveloperEdition.png](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/media/change-sql-server-edition/edition-change-in-portal.png) 

## **Recommended Documents**

* [Upgrade to a different edition - SQL Server](https://docs.microsoft.com/sql/database-engine/install-windows/upgrade-to-a-different-edition-of-sql-server-setup?view=sql-server-ver15)
