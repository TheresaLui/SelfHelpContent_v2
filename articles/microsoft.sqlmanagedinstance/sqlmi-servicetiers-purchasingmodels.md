<properties
	pageTitle="Service tiers|Purchasing models"
	description="Service tiers|Purchasing models"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637295,32637294"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    articleId="9372d04b-2250-4ff5-8587-00b9afa9ff1d"
	ownershipId="AzureData_AzureSQLMI"
/>

# Purchasing models

Managed instance is purchased through a monthly subscription. Backup storage above the allocated amount is charged per usage.

- Discounts are provided for existing on-premises SQL Server license owners through the program called Azure Hybrid Benefit
- Reserved capacity allows discounts based on 1 or 3 year purchase commitment
- Enterprise dev/test subscription types are eligible for discounts
- Instance pools deployment option is available for customers who need to deploy multiple managed instances with non-intensive workloads

## **Recommended Steps**

**Standard purchasing model**

- The charge for managed instance is billed monthly based on these billing metrics:

	- [Service tier](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-service-tiers)
	- Number of vCores
	- Data storage space
	- Backup storage used above the free tier

- Backup storage is provided free of charge in the same amount as data storage space purchased. For example, if you have purchased 4TB of data storage, the same amount of up to 4TB of backup storage will be provided for free. If your backup storage consumption goes above 4TB in this example, there is a surcharge for backup storage used above the free tier.

**Discounts**

- For existing SQL server license owners, existing licenses can be applied to obtain a discount for managed instance. To learn more, see [Azure Hybrid Benefit](https://azure.microsoft.com/pricing/hybrid-benefit/). This discount is applied at the time you create managed instance through an available configuration option. In addition, the license discount can also be applied once managed instance is created through the pricing tier blade in portal.
- For prepayments of SQL Database compute resources in duration of 1 or 3 years, discounts are available. To learn more, see [Azure SQL Database reserved capacity](https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity). This option is purchased from Azure portal, go to All services > Reservations, then Add and chose SQL Database. Once reserved capacity is purchased, when you create managed instance afterwards, the compute discount will be automatically applied and reflected in the price shown.
- For enterprise customers using Enterprise Dev/Test subscriptions, discounts are automatically applied for the cost of SQL licenses. In other words, for customers using this type of subscription no license costs are charged for managed instance automatically. To learn more, see [Enterprise Dev/Test subscriptions](https://azure.microsoft.com/offers/ms-azr-0148p/).

**Deployments at scale**

- For customers who need to deploy multiple managed instances, option of provisioning instance pools might be cost beneficial. Instance pool is pre-provisioned capacity from 8 up to 80 vCores in which multiple managed instances of various sizes can be packed. This is the only option offering the smallest 2 vCore managed instances (not available as standalone managed instances otherwise). For example, with instance pools it is possible to pack 40 x 2 vCore managed instances in 80 vCores instance pool. If this deployment option is used, the billing for compute (vCores) is per individual instance pool. Storage is billed separately for each separate managed instance placed in an instance pool. To learn more, see [QL Database instance pools](https://docs.microsoft.com/azure/sql-database/sql-database-instance-pools).

## **Recommended Documents**

- [Managed instance service tiers](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-service-tiers)
- [Azure Hybrid Benefit](https://azure.microsoft.com/pricing/hybrid-benefit/)
- [Azure SQL Database reserved capacity](https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity)
- [Enterprise Dev/Test subscriptions](https://azure.microsoft.com/offers/ms-azr-0148p/)
- [SQL Database instance pools](https://docs.microsoft.com/azure/sql-database/sql-database-instance-pools)
