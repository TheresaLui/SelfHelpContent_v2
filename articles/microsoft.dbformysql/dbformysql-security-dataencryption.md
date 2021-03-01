<properties
    pageTitle="Data encryption for Azure Database for MySQL"
    description="Data encryption for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="bahusse"
    ms.author="manishku"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32738655"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="58c25acb-f733-4eb3-a0a1-b2972e47ff25"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Data encryption in Azure Database for MySQL

Data encryption with customer-managed keys for Azure Database for MySQL enables you to bring your own key (BYOK) for data protection at rest. It also allows organizations to implement separation of duties in the management of keys and data. With customer-managed encryption, you are responsible for (and in full control of) a key's lifecycle, usage permissions, and auditing of operations on keys. Learn more about [Data encryption](https://docs.microsoft.com/azure/mysql/concepts-data-encryption-mysql).

**NOTE**: This functionality is currently only supported in Azure Database for MySQL Single server.

## **Recommended Steps**

* **Data encryption** is only available for the **General purpose** and **Memory optimized** SKU
* For your General purpose and Memory optimized SKUs that do not have data encryption, ensure that your server has [large storage](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage)
* Set **Data encryption** for your Azure Database for MySQL from either:
    * [The Azure portal](https://docs.microsoft.com/azure/mysql/howto-data-encryption-portal)
    * [CLI](https://docs.microsoft.com/azure/mysql/howto-data-encryption-cli)
* This feature is only supported in regions and servers that support storage up to 16TB. Refer to [this note](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage).
* Encryption is only supported with an RSA 2048 cryptographic key

* **Why Data Encryption is not available for my Azure Database for MySQL server?** 

   Support for this functionality is limited to General Purpose and Memory Optimized pricing tiers and is only supported in regions and servers that support storage up to 16 TB. Read more on [MySQL data encryption Limitations](https://docs.microsoft.com/azure/mysql/concepts-data-encryption-mysql#limitations).

## **Recommended Documents**

* [Data encryption](https://docs.microsoft.com/azure/mysql/concepts-data-encryption-mysql)
* [Data encryption - Portal](https://docs.microsoft.com/azure/mysql/howto-data-encryption-portal)
* [Data encryption - CLI](https://docs.microsoft.com/azure/mysql/howto-data-encryption-cli)
