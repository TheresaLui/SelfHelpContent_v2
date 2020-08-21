<properties
	pageTitle="availability and connectivity/My database isn't listed in the Azure portal"
	description="availability and connectivity/My database isn't listed in the Azure portal"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630436"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="58670c80-142f-4d91-820e-12beeafc0d8f"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# availability and connectivity/My database isn't listed in the Azure portal

## **Recommended Steps**

Try connecting to your server/database using one of the client tool(s) (SQL Management Studio, Visual Studio, or Other). <br>

### If database is unreachable<br>

* To find out who dropped the database please use operation logs and then [recover your database from backups](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups?WT.mc_id=pid:13491:sid:32630436/).<br>

### If database is accessible<br>

* Open a support ticket for this problem.
