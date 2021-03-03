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
1. Please take the VM SnapShot backup also have Database backup
2. Provision a VM  from Azure market Place with Sql 2017 Developer Edition . Or you can Download the developer Edition from Microsoft Download center.
3. Copy the Setup file from Path  (C:SqlServerFull) to Sql 2017 Express edition (Old)
4. Go to Maintenance -> Edition Upgrade
![EditionUpgrade.png](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/media/change-sql-server-edition/edition-upgrade.png) 
5.  From Portal -> Under setting->Configure  please change the Edition to developer
![PortalDeveloperEdition.png](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/media/change-sql-server-edition/edition-change-in-portal.png) 

## **Recommended Documents**

* [Upgrade to different edition - SQL Server](https://docs.microsoft.com/sql/database-engine/install-windows/upgrade-to-a-different-edition-of-sql-server-setup?view=sql-server-ver15)
