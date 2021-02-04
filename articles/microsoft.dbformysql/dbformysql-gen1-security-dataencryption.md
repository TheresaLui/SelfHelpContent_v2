<properties
  pagetitle="Data encryption in Azure Database for MySQL&#xD;"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse,pariks"
  selfhelptype="Generic"
  supporttopicids="32747554"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="04cfd820-a233-4d7a-b4a7-ef670bfb7d37"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Data encryption in Azure Database for MySQL

Data encryption with customer-managed keys for Azure Database for MySQL enables you to bring your own key (BYOK) for data protection at rest. 

**Error**
Customer encryption key for data encryption on Azure MySQL is not working when enabled using Azure-CLI:
key "xxxx" is not valid. Please ensure the key vault has been configured with soft-delete.

## **Recommended Steps**

### Data Encryption

* The key must have the following attributes to use as a customer-managed key:

 * No expiration date
 * Not disabled
 * Perform get, wrap, unwrap operations
 * Soft delete enabled with retention days set to 90 days
 * Purge protection enabled

To see if the preceding requirements are met, verify key attributes with the following command:

```
az keyvault key show --vault-name keyVaultName -n keyName
```

* **Data encryption** is available only for the **General purpose** and **Memory optimized** SKUs
* If your General purpose and Memory optimized SKU does not have data encryption, ensure that your server has [large storage](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage) that supports up to **16TB**.
* You can set **Data encryption** for your Azure Database for MySQL from [the portal](https://docs.microsoft.com/azure/mysql/howto-data-encryption-portal)
* You can set **Data encryption** for your Azure Database for MySQL from [CLI](https://docs.microsoft.com/azure/mysql/howto-data-encryption-cli)
* Encryption is supported only with the RSA 2048 cryptographic key

### Infrastructure double Encryption
* **Infrastructure double Encryption** is only available for the **General purpose** and **Memory optimized** SKU
* For your General purpose and Memory optimized SKU does not have data encryption, ensure that your server has [large storage](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers#storage)
* You can set **Infrastructure double Encryption** for your Azure Database for MySQL from [the portal](https://docs.microsoft.com/azure/mysql/howto-double-encryption)
* Currently, this feature supported only in East US, South Central US, and West US. For more information, see [limitations](https://docs.microsoft.com/azure/mysql/concepts-infrastructure-double-encryption#limitations).

* **Why Data Encryption is not available for my Azure Database for MySQL server?** Please note that Support for this functionality is limited to General Purpose and Memory Optimized pricing tiers and **only** supported in regions and servers which support storage up to 16TB. Read more on [MySQL data encryption Limitations](https://docs.microsoft.com/azure/mysql/concepts-data-encryption-mysql#limitations).

## **Recommended Documents**

* [Data encryption](https://docs.microsoft.com/azure/mysql/concepts-data-encryption-mysql)
* [Data encryption - portal](https://docs.microsoft.com/azure/mysql/howto-data-encryption-portal)
* [Data encryption - CLI](https://docs.microsoft.com/azure/mysql/howto-data-encryption-cli)
