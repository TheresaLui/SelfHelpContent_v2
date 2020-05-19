<properties
	pageTitle="Database in the inaccessible state - Key Vault Deleted"
	description="Database in the inaccessible state due to the AKV vault being deleted"
	infoBubbleText="Database is in the inaccessible state due to the AKV vault being deleted. See recommended actions on the right."
	service="microsoft.sql"
	resource="servers"
	authors="nikolasoggMSFT"
	ms.author="niogg"
	displayOrder=""
	articleId="IsDBInaccessibleKeyVaultDeleted_C205F2D0-7AAB-4C50-B9B2-AF699A53A2B8"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="32630405, 32630429, 32630438, 32637230"
	resourceTags=""
	productPesIds="13491, 16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# Database Inaccessible due to Azure Key Vault configuration - Key Vault Deleted

## We ran diagnostics on your resource and found an issue
<!--issueDescription-->
Your database **<!--$DatabaseName--> DatabaseName <!--/$DatabaseName-->** is in the "Inaccessible" state due to the Azure Key Vault being deleted. To resolve this issue, restore the vault and key required by the server's transparent data encryption configuration.

The affected key has URI <!--$AzureKeyVaultUri-->AzureKeyVaultUri<!--/$AzureKeyVaultUri-->
<!--/issueDescription-->

## Inaccessible Database State
When transparent data encryption (TDE) is configured to use a customer-managed key, continuous access to the TDE protector is required for the database to stay online. When the server loses access to the customer-managed TDE protector in Azure Key Vault (AKV), in up to 10 minutes the database will start denying all external user connections and the database state will become "Inaccessible". The only action allowed on the database in the "Inaccessible" state is to make it accessible again after restoring access to the key or dropping the database if that is the intent.

After access to the key is restored, taking database back online requires additional steps, which may vary based on the time elapsed without access to the key and the size of the database.

* If key access is restored within 8 hours, the database will auto-heal and become accessible
* If key access is restored after 8 hours, auto-heal is not possible and bringing the database might take time depending on the size of the database and requires opening a support ticket. Once the database is back online, previously configured server-level settings such as failover group configuration, point-in-time-restore history, and tags will be lost.

## **Recommended Steps**

Key access can be lost for multiple reasons such as:

* Deletion of the key or key vault - to fix, ensure the key vault and the key exist
* Revoked permissions to the key:

	* Ensure the SQL Server instance AppId has sufficient permissions to access the key and key vault. At minimum 'Get, WrapKey, UnwrapKey' permissions are required.
	* Ensure the Key vault key permission has sufficient permission to perform Wrap and Unwrap permission
	* Ensure that the key vault key is not expired
	* Ensure that the key vault key is not disabled
    	* Ensure that the firewall setting is correct
    	* Ensure that the APPId still exists in the AAD Tenant

Additional causes and solutions can be found [here](https://docs.microsoft.com/sql/relational-databases/security/encryption/troubleshoot-tde?view=azuresqldb-current).

## **Recommended Documents**
* [**Inaccessible TDE Protector**](https://docs.microsoft.com/azure/sql-database/transparent-data-encryption-byok-azure-sql#inaccessible-tde-protector): Additional information about the inaccessible state
* [**Common errors for transparent data encryption with customer-managed keys in Azure Key Vault**](https://docs.microsoft.com/sql/relational-databases/security/encryption/troubleshoot-tde?view=azuresqldb-current): Additional causes and mitigations for an inaccessible database

