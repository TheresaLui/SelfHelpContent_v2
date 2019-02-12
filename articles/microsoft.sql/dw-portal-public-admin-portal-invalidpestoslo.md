  <properties
	pageTitle="Can't scale Gen2 DW below DW500c"
	description="Can't scale Gen2 DW below DW500c"
	service="microsoft.sql"
	resource="servers"
	authors="tomfalko"
	ms.author="tomfalko"
	displayOrder="11"
	selfHelpType="resource"
	supportTopicIds="32412136"
	resourceTags="datawarehouse"
	productPesIds="15818"
	cloudEnvironments="public"
	articleId="f48635af-1630-4674-8ccb-8a79dbdf4f5a"
/>

# Gen2 Service Level Objectives (SLO)

## Error: Gen2 SLOs below DW500c not available

DW500c is the smallest Gen2 SLO available. 

In some Azure regions, the Portal will allow you to select a SLO below DW500c. This is a bug that is being corrected. If an SLO smaller than DW500c is selected, the scale operation will fail.

## **Recommended Documents**

* [Gen2 SLOs](https://azure.microsoft.com/pricing/details/sql-data-warehouse/gen2/)
* [Memory and concurrency limits for Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/memory-and-concurrency-limits)
