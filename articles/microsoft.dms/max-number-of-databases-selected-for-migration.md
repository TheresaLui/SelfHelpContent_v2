<properties
	pageTitle="Max number of databases selected for migration"
	description="Recommendation and information for troubleshooting  DMS activity creation and deletion"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="service-create-or-delete-failure"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32673593"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public"
/>

# Recommendation and information for troubleshooting  DMS activity creation and deletion

## **Recommended Steps**

**Error:**
* *"Service has reported errors when trying to migrate more than 4DBs per service."*<br>

### **Recommended Steps** 

* The Service can only migrate 4 DBs concurrently and you can have 2 service per subspcription.
* DMS only supports 4 DBs to migrate concurrently. It allows you to create many projects, for example, you create 10 projects and select 4 databases in each. Although you have 40 Dbs but only 4 of them will be migrated at one time.
* Another limit is per sub, per region, only 2 DMS services are allowed to create, which means you will have 8 Dbs to migrate concurrently at one time.