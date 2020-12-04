<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783876"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Administration and Security/Dedicated SQL pool - Transparent Data Encryption (TDE)"
    description = "Administration and Security/Dedicated SQL pool - Transparent Data Encryption (TDE)"
    articleId = "synapse-cs-administrationandsecurity-dedicatedsqlpooltransparentdataencryptiontd.md"
    ms.author = "saltug,goventur"
/>

# Administration and Security/Dedicated SQL pool - Transparent Data Encryption (TDE)

## **Recommended Steps**

* **Is TDE enabled by default for Azure Synapse databases?**
   - Databases in Azure Synapse are not encrypted by default. TDE encryption configuration is not inherited from server level.

* **Performance impact of enabling TDE**
   - To enable TDE on a database, Synapse must do an encryption scan that reads each page from the data files into the buffer pool and then writes the encrypted pages back to disk
   - The performance impact of TDE varies with the type of data you have, how it is stored, and the type of workload activity on the database. When protected by TDE, the I/O of reading and then decrypting data, or the encrypting and then writing data, are CPU intensive activities and will have more impact when other CPU intensive activities are happening at the same time.

* **Recommendations before enabling TDE encryption:**
   
   - Review the health of any Clustered Columnstore Indexes to maximize compression and remove any deleted records
   - Fragmentation of objects means more pages to read and encrypt, consider rebuilding them before enabling TDE
   - More information about [Columnstore indexes](https://docs.microsoft.com/sql/relational-databases/indexes/columnstore-indexes-overview?view=azure-sqldw-latest), how to [improve columnstore index performance](https://docs.microsoft.com/azure/synapse-analytics/sql/data-load-columnstore-compression), and [detecting and resolving fragmented indexes](https://docs.microsoft.com/sql/relational-databases/indexes/reorganize-and-rebuild-indexes?view=azure-sqldw-latest)
   - If possible, enable TDE during a time window with minimal workload to avoid contention as some DML operations can be blocked and CRUD operations can be delayed as well
   - Consider temporarily increasing the SLO of your Synapse SQL Pool instance when enabling TDE encryption, it can help to complete the process faster since there will be more compute nodes available to perform the encryption, once TDE is enabled the SLO configuration can be reverted (beware of additional costs when increasing the SLO)
   
* **Can I cancel the TDE encryption scan before it completes?**
   - There is no option to pause or cancel TDE encryption scan after it is initiated. Once the encryption scan completes, you may disable TDE again.

* **TDE progress bar is not updating in the Azure portal**
   - As an alternative, you can view the state of TDE via [PowerShell](https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption?toc=%2Fazure%2Fsynapse-analytics%2Fsql-data-warehouse%2Ftoc.json&bc=%2Fazure%2Fsynapse-analytics%2Fsql-data-warehouse%2Fbreadcrumb%2Ftoc.json&view=azps-4.6.0)

* **Monitoring TDE encryption process:**
   - Run the following SQL query to monitor the encryption state:

```
        SELECT D.database_id AS DBIDinMaster, D.name AS UserDatabaseName,  
        PD.pdw_node_id AS NodeID, DM.physical_name AS PhysDBName,  
        keys.encryption_state 
        FROM sys.dm_pdw_nodes_database_encryption_keys AS keys 
        JOIN sys.pdw_nodes_pdw_physical_databases AS PD 
            ON keys.database_id = PD.database_id AND keys.pdw_node_id = PD.pdw_node_id 
        JOIN sys.pdw_database_mappings AS DM 
            ON DM.physical_name = PD.physical_name 
        JOIN sys.databases AS D 
            ON D.database_id = DM.database_id 
        ORDER BY D.database_id, PD.pdw_node_ID;
```

* **DMVs to monitor the state of encryption:**

   - [sys.dm_pdw_nodes_database_encryption_keys](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-pdw-nodes-database-encryption-keys-transact-sql?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json&view=azure-sqldw-latest)

   - [sys.databases](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-databases-transact-sql?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json&view=azure-sqldw-latest)

## **Recommended Documents**

* **How-to guides:**
   - [Manage TDE using the Portal](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-encryption-tde)

   - [Manage TDE using T-SQL](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-encryption-tde-tsql)

* **More Information:**
   - [Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=azure-sqldw-latest)

   - [Transparent data encryption for Azure Synapse Analytics](https://docs.microsoft.com/azure/azure-sql/database/transparent-data-encryption-tde-overview?tabs=azure-portal#manage-transparent-data-encryption)
   
   - [TDE with Bring Your Own Key](https://docs.microsoft.com/azure/azure-sql/database/transparent-data-encryption-byok-overview)

 