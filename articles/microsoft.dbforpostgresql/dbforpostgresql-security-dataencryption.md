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

# Data encryption with customer-managed key (CMK) in Azure Database for PostgreSQL - Single server

Azure PostgreSQL leverages Azure Storage encryption to encrypt data at-rest using Microsoft-managed keys. This default setting is enabled from the moment your server is created and can't be disabled.

Data encryption with customer-managed keys for Azure Database for PostgreSQL enables you to bring your own key (BYOK)---also known as a Customer Managed Key (CMK)---for data protection at rest. It also allows organizations to implement separation of duties in the management of keys and data. With customer-managed encryption, you are responsible for, and in a full control of, a key's lifecycle, key usage permissions, and auditing of operations on keys. Learn more about [Data encryption with CMK](https://docs.microsoft.com/azure/postgresql/concepts-data-encryption-postgresql).

You can use infrastructure double-encryption for a second layer of encryption using service-managed keys.

## **Recommended steps**

**Are you trying to confirm whether data is encrypted in Azure Database for PostgreSQL?**
* Data is always encrypted in Azure Database for PostgreSQL - Single server (data, logs, backups, etc.) It is mandatory and can't be turned off. 
* Customer managed key (CMK) is a feature that allows you to be in full control of the encryption key.

**Are you looking for a way to enable customer-managed key (CMK) for data encryption on your server but can't find it?**
* Check that you are not using Basic tier. CMK for data encryption is only available for the **General purpose** and **Memory optimized** tiers.
* If you are using General purpose or Memory optimized tier, ensure that your server has [large storage up to 16 TB](https://docs.microsoft.com/azure/postgresql/concepts-pricing-tiers#storage). If your server is not enabled for large storage, you would need to create a new server with large storage and migrate your original database to use CMK for data encryption.

**Do you need to find steps to enable CMK for data encryption on your server?**
* You can enable CMK for your Azure Database for PostgreSQL from the [portal](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-portal).
* You can enable CMK for your Azure Database for PostgreSQL from [CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli).

**Do you need to find information about strength of CMK?**<br>
Encryption is only supported with the RSA 2048 cryptographic key.

**Are you looking for a way to setup key auto-rotation?**<br>
You can set auto-rotation of the CMK in Azure Key Vault, but after the key is rotated, you must explicitly change the new version of the key for the Server by using the portal or the Create CLI command described in [Create CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli#set-data-encryption-for-azure-database-for-postgresql-single-server).

**Do you need to enable [double encryption](https://docs.microsoft.com/azure/postgresql/concepts-infrastructure-double-encryption) on your server?**<br>
You can enable infrastructure double encryption for Azure Database for PostgreSQL - Single server at create time [in portal or using CLI](https://docs.microsoft.com/azure/postgresql/howto-double-encryption)
    
## **Recommended documents**

* [Data encryption fundamentals in Azure Database for PostgreSQL - Single server](https://docs.microsoft.com/azure/postgresql/concepts-security#information-protection-and-encryption)
* [Data encryption with CMK in Azure Database for PostgreSQL - Single server](https://docs.microsoft.com/azure/postgresql/concepts-data-encryption-postgresql)
* [Data encryption with CMK - Portal](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-portal)
* [Data encryption with CMK - CLI](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-cli)
* [Validating data encryption with CMK](https://docs.microsoft.com/azure/postgresql/howto-data-encryption-validation)
* [Data encryption - Azure KeyVault](https://azure.microsoft.com/services/key-vault)
* [Infrastructure double encryption](https://docs.microsoft.com/azure/postgresql/concepts-infrastructure-double-encryption)

