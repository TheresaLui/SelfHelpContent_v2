<properties
	pageTitle="Create/Scale/Pause/Resume/Delete/Cannot scale higher or lower"
	description="Create/Scale/Pause/Resume/Delete/Cannot scale higher or lower"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw,anvang"
	supportTopicIds="32635190"
	productPesIds="15818"
	displayOrder=""
	selfHelpType="generic"
	resourceTags=""
	articleId="dw-createscalepauseresumedelete-cannotscalehigherorlower.md"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Cannot scale higher or lower

If you are unable to scale higher, it is usually due to DTU quota limits on the server (the service level not being available in the region). 

If you are unable to scale lower, it is usually because some lower service levels (below DWU500c) are not yet available on Gen2. Check the [Gen2 Regional Availability Schedule](https://docs.microsoft.com/azure/sql-data-warehouse/gen2-migration-schedule) to determine when these service levels will be available in your region.

## **Recommended Documents**

* [Pricing Page](https://azure.microsoft.com/pricing/details/sql-data-warehouse/gen2/) (prices only show live regions and service levels)<br>
* [Gen2 Regional Availability Schedule](https://docs.microsoft.com/azure/sql-data-warehouse/gen2-migration-schedule)<br>
* [DTU quota limits](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-service-capacity-limits)<br>
* [Scale from Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-portal)<br>
* [Scale from PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-powershell)<br>
* [Scale from T-SQL](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-tsql)<br>
* [Permissions for scaling SQL Pools](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-manage-compute-overview#permissions)
