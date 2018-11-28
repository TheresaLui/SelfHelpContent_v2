  <properties
	pageTitle="Can't scale Gen2 DW below DW500c"
	description="Can't scale Gen2 DW below DW500c"
	service="microsoft.sql"
	resource="servers"
	authorAlias="tomfalko"
	displayOrder="11"
	selfHelpType="resource"
	supportTopicIds="32412136"
	resourceTags="datawarehouse"
	productPesIds="15818"
	cloudEnvironments="public"
/>

# Gen2 SLOs

## Gen2 SLOs below DW500c not available
DW500c is the smallest Gen2 SLO you can use.  

In some Azure regions, the Portal will allow one to select a SLO below DW500c.  This is a bug that is being corrected.  If one selects an SLO smaller than DW500c, the scale operation will fail.

## **Recommended documents**

[Gen2 SLOs](https://azure.microsoft.com/pricing/details/sql-data-warehouse/gen2/)
[Memory and concurrency limits](https://docs.microsoft.com/azure/sql-data-warehouse/memory-and-concurrency-limits)
