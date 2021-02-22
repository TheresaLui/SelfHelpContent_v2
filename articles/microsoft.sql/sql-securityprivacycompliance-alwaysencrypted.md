<properties
	pageTitle="Always Encrypted & Always Encypted with Secure Enclaves"
	description="Always Encrypted & Always Encypted with Secure Enclaves Self help"
	service="microsoft.sql"
	resource="servers"
	authors="pookam"
    ms.author="pookam"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32782210"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="7a96712e-bc01-4711-bfea-97900707cd67"
	ownershipId="AzureData_AzureSQLDB"
/>

# Always Encrypted

[Always Encrypted](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-database-engine?view=sql-server-ver15) protects sensitive data from malware and high-privilege unauthorized users, including database administrators and cloud database operators. It supports simple confidential computations, including point lookup searches and equality joins, by leveraging deterministic encryption.

[Always Encrypted with secure enclaves](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-with-secure-enclaves-landing) extends Always Encrypted by providing richer confidential computing capabilities, including in-place encryption, pattern matching, range comparisons, and sorting.
It leverages server-side, secure enclaves and does not rely on deterministic encryption to support confidential computations.

Most users are able to resolve their issues related to Always Encrypted by using the following steps.

## **Recommended Steps**

  1. To use **Always Encrypted with secure enclaves**, create your resource group in a region that supports the DC-series hardware configuration. For the list of currently supported regions, see [DC-series](https://docs.microsoft.com/azure/azure-sql/database/service-tiers-vcore?tabs=azure-portal#dc-series).
  Get Started with Always encrypted with secure enclaves with this [Tutorial](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-enclaves-getting-started)
  
   2. Before you can use **Always Encrypted with secure enclaves**, you must configure your environment to ensure that the secure enclave is available for the database. You also need to set up enclave attestation. The attestation of Intel SGX enclaves in Azure SQL Database requires [Microsoft Azure Attestation](https://docs.microsoft.com/azure/attestation/overview).
   
   2. Errors can occur at various steps of the above workflow due to misconfigurations. Here are the common attestation errors, their root causes, and the recommended troubleshooting steps: [Troubleshoot common issues when running statements using Enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-enclaves-query-columns?view=sql-server-ver15#troubleshoot-common-issues-when-running-statements-using-enclaves) 

   3. Check if you are running into [Known Limitations for Always Encrypted with Secure Enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-enclaves?view=sql-server-ver15#known-limitations)
      * For additional limitations of Always Encrypted and Always Encrypted with secure enclaves, see [Feature Details](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-database-engine?view=sql-server-ver15#feature-details).
 
## **Recommended Documents**

* Always Encrypted:

   * [Feature Limitations](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-database-engine?view=sql-server-ver15#feature-details)
   * [Configure Always Encrypted using PowerShell](https://docs.microsoft.com/sql/relational-databases/security/encryption/configure-always-encrypted-using-powershell?view=sql-server-ver15)
   * [Configure Always Encrypted using Key Vault](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-azure-key-vault-configure?view=sql-server-ver15&tabs=azure-powershell)
   * [Overview of Key Management](https://docs.microsoft.com/sql/relational-databases/security/encryption/overview-of-key-management-for-always-encrypted?view=sql-server-ver15)
   * [Configure desired encryption for columns](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-wizard?view=sql-server-ver15)
   * [Always Encrypted Cryptography](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-cryptography?view=sql-server-ver15)
   * [Provision and rotate cryptographic keys for Always Encrypted](https://docs.microsoft.com/sql/relational-databases/security/encryption/create-and-store-column-master-keys-always-encrypted?view=sql-server-ver15)
   * [Query columns using Always Encrypted with SQL Server Management Studio](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-query-columns-ssms?view=sql-server-ver15)
   * [Migrate data stored in encrypted columns or databases using Always Encrypted](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-migrate-using-bacpac?view=sql-server-ver15)
   * [Develop applications and learn which drivers support Always Encrypted](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-client-development?view=sql-server-ver15)

* Always Encrypted with secure enclaves:

  * [Set up the secure enclave and attestation in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/always-encrypted-enclaves-getting-started)
  * [Run Transact-SQL statements using secure enclaves](https://docs.microsoft.com//sql/relational-databases/security/encryption/configure-always-encrypted-enclaves?view=sql-server-ver15#run-transact-sql-statements-using-secure-enclaves)
  * [Manage keys for Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/configure-always-encrypted-enclaves?view=sql-server-ver15#manage-keys-for-always-encrypted-with-secure-enclaves)
  * [Create and use indexes on enclave-enabled columns](https://docs.microsoft.com/sql/relational-databases/security/encryption/configure-always-encrypted-enclaves?view=sql-server-ver15#create-and-use-indexes-on-enclave-enabled-columns)
  * [Develop applications using Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/configure-always-encrypted-enclaves?view=sql-server-ver15#develop-applications-using-always-encrypted-with-secure-enclaves)
  * [Configure columns with Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/configure-always-encrypted-enclaves?view=sql-server-ver15#configure-columns-with-always-encrypted-with-secure-enclaves)
  * [Troubleshoot common issues when running statements using enclaves](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-enclaves-query-columns?view=sql-server-ver15#troubleshoot-common-issues-when-running-statements-using-enclaves) 
  
