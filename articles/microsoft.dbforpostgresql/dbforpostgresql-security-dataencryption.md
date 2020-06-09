<properties
    pageTitle="Data encryption for Azure Database for PostgreSQL"
    description="Data encryption for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32740814"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8cca194a-0a92-4c0e-930a-5ab434002c94"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Data encryption in Azure Database for PostgreSQL

Data encryption with customer-managed keys for Azure Database for PostgreSQL enables you to bring your own key (BYOK) for data protection at rest. It also allows organizations to implement separation of duties in the management of keys and data. With customer-managed encryption, you are responsible for, and in a full control of, a key's lifecycle, key usage permissions, and auditing of operations on keys. Learn more about [Data encryption](https://docs.microsoft.com/azure/postgresql/concepts-data-encryption-postgresql).

## **Recommended Steps**

* **Data encryption** is only available for the **General purpose** and **Memory optimized** SKU
* For your General purpose and Memory optimized SKU does not have data encryption, please ensure that your server has [large storage](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#storage)
* You can set **Data encryption** for your Azure Database for PostgreSQL from [portal](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-portal)
* You can set **Data encryption** for your Azure Database for PostgreSQL from [CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli)
* This feature is only supported in regions and servers which support storage up to 16TB. Please refer to the note [here](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#storage).
* Encryption is only supported with RSA 2048 cryptographic key

## **Recommended Documents**

* [Data encryption](https://docs.microsoft.com/azure/postgresql/concepts-data-encryption-postgresql)
* [Data encryption - Portal](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-portal)
* [Data encryption - CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli)
