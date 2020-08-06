<properties
	pageTitle="Create or Drop Resources/Instance Pools"
	description="Create or Drop Resources/Instance Pools"
    infoBubbleText="Create or Drop Resources/Instance Pools"
	service="microsoft.sql"
	resource="servers"
	authors="urosmil"
	ms.author="urmila"
	displayOrder=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32674897"
    resourceTags=""	
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="6c7a079b-439d-4850-a8ea-f7fe24fdf9f9"
	ownershipId="AzureData_AzureSQLMI"
/>

# Create or drop instance pools

Instance pools allow you to pre-provision compute resources according to your total migration requirements. You can then deploy several individual managed instances up to your pre-provisioned compute level.

There are several resource limitations regarding instance pools and instances inside pools:

- Instance pools are available only on Gen5 hardware
- Instances within a pool have dedicated CPU and RAM, so the aggregated number of vCores across all instances must be less than or equal to the number of vCores allocated to the pool
- All instance level limits apply to instances created within a pool
- In addition to instance-level limits there are also two limits imposed at the instance pool level: 

	- Total storage size per pool (8 TB)
	- Total number of databases per pool (100)

Deployment of instance pools can be managed only using PowerShell during public preview. Things to be aware of that are related to instance pool creation are:

- Creating instance pool is long running operation
- Creating instance pool is not cancelable operation

## **Recommended Steps**

For more info on instance pools: 

- Read what are SQL Database [instance pools](https://docs.microsoft.com/azure/sql-database/sql-database-instance-pools)
- Check list of commands in [how-to guide](https://docs.microsoft.com/azure/sql-database/sql-database-instance-pools-how-to)
- Deployment duration of instance pool is similar to [deployment time of single instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)

## **Recommended Documents**

- What are SQL Database [instance pools](https://docs.microsoft.com/azure/sql-database/sql-database-instance-pools)
- Instance pools [how-to guide](https://docs.microsoft.com/azure/sql-database/sql-database-instance-pools-how-to)
