<properties
pageTitle="How to have better restore performance and monitor restore progress"
description="How to have better restore performance and monitor restore progress"
ms.author="vtpombei"
displayOrder=""
articleId="099B07DD-23DC-458E-8EEF-177B712BD84E"
selfHelpType="Apollo"
supportTopicIds=""
productPesIds="13491"
cloudEnvironments="public"
mappedToBucket="true"
ownershipId="AzureData_AzureSQLDB"
/>

# How to have better restore performance and monitor restore progress

## How to have better restore performance

- The size and activity of the database.
    - As expected the bigger the database the longer the restore will take.
        - Reduce the non-clustered indexes that are not being used or that can be merged with another non-clustered index.
    - Database with high write activity will have bigger diff and log backups that needs to be replayed to recover to the restore point.
        - Avoid doing frequently indexes maintenance, work only on the indexes that really require maintenance.
 
- The service tier of the target Azure SQL Database
    - Using a higher service tier for a faster restore process then scale to the intended service tier
    - Use a service tier with better storage performance like Premium or Business Critical
    - Avoid using Basic, S0 or S1 as they use Azure Standard Storage that is less performance
    - Consider restoring the Azure SQL Database as a single database and them move it to an Elastic Pool if that is the final destination
    - Note: The billing will start when the Azure SQL Database is available

- Avoid having long running transactions
    - Azure SQL Database engine guarantees that the whole database is logically consistent after the restore process for the database to be brought online.
    - If the point in time provided has high number of active long running transactions they will have to be rollback.

- Select the same Azure region as the original Azure SQL Database or paired region
    - This will avoid sending the restore data through network to another Azure region.
    - For geo-restore confirm that the destination Azure region is the [paired region](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) of the original Azure SQL Database to avoid sending the restore data throw network.

- The number of concurrent restore requests being processed in the target region
    - If there is a prolonged outage in a region, it's possible that a high number of geo-restore requests will be initiated for disaster recovery. When there are many requests, the recovery time for individual databases can increase.
    - For a single subscription, there are limitations on the number of concurrent restore requests. These limitations apply to any combination of point-in-time restores, geo-restores, and restores from long-term retention backup.

|Deployment option|Max # of concurrent requests being processed|Max # of concurrent requests being submitted|
|--|:--:|:--:|
|Single database (per subscription)|30|100|
|Elastic pool (per pool)|4|2000|

## How to monitor restore requests

To monitor the progress of a restore request use the following T-SQL statement.

```
SELECT major_resource_id, percent_complete
FROM sys.dm_operation_status
WHERE operation LIKE '%DATABASE RESTORE%'
```


## How to avoid having restore requests getting stuck

- Confirm that the service tier selected as the target can handle the storage needed for the Azure SQL Database.
- When restoring to an Elastic Pool confirm that it has enough storage available for the database being restore.
    - Consider restoring the Azure SQL Database as a single database and them move it to the Elastic Pool
