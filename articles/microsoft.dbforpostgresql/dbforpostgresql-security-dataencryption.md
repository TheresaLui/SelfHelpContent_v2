<properties
    pageTitle="Data encryption for Azure Database for PostgreSQL"
    description="Data encryption for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32740814, 32780950"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8cca194a-0a92-4c0e-930a-5ab434002c94"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Data encryption in Azure Database for PostgreSQL

Data encryption with customer-managed keys for Azure Database for PostgreSQL enables you to bring your own key (BYOK), also known as a Customer Managed Key (CMK), for data protection at rest. It also allows organizations to implement separation of duties in the management of keys and data. With customer-managed encryption, you are responsible for, and in a full control of, a key's lifecycle, key usage permissions, and auditing of operations on keys. Learn more about [Data encryption](https://docs.microsoft.com/azure/postgresql/concepts-data-encryption-postgresql).

## **Recommended Steps**

* **Data encryption** is only available for the **General purpose** and **Memory optimized** SKU
* For your General purpose and Memory optimized SKU that doesn't have data encryption, ensure that your server has [large storage](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#storage). If your server is not enabled for large storage, you must create a new server with large storage and migrate your original database
* You can set **Data encryption** for your Azure Database for PostgreSQL from the [portal](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-portal)
* You can set **Data encryption** for your Azure Database for PostgreSQL from [CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli)
* This feature is only supported in regions and servers that support storage up to 16 TB. See [additional details](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#storage).
* Encryption is only supported with the RSA 2048 cryptographic key
* You can set auto-rotation of the CMK in Azure Key Vault, but after the key is rotated, you must explicitly change the new version of the key for the Server by using the portal or the Create CLI command described in [Create CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli#set-data-encryption-for-azure-database-for-postgresql-single-server)

## **Recommended Documents**

* [Data encryption](https://docs.microsoft.com/azure/postgresql/concepts-data-encryption-postgresql)
* [Data encryption - Portal](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-portal)
* [Data encryption - CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli)
* [Data encryption - Azure KeyVault](https://azure.microsoft.com/services/key-vault)
