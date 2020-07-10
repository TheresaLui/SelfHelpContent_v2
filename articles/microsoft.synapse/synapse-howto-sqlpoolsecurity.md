<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738825"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "How-To/SQL pool security"
	description = "How-To/SQL pool security"
	articleId = "synapse-howto-sqlpoolsecurity"
	authors = "saltug"
	ms.author = "saltug"
/>

# How-To/SQL pool security

## **Recommended Steps**

The following details explain how to set up and update common access and permissions rules in SQL pool.

* If you're looking to change the administrator password for a logical SQL Server, you can simply click "Reset Password" at the top of the SQL Server resource blade
* [Configure SQL firewall rules](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-get-started-provision/#create-a-new-azure-sql-server-level-firewall) for the IP addresses that are authorized to access this SQL pool
* To set-up and connect to SQL pool using [Azure Active Directory](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-authentication/) authentication
* [Secure your SQL pool](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)

### What access control can be done at the server level

* Server-level permissions are not available in Synapse SQL. For more information, see [Using fixed and custom database roles](https://docs.microsoft.com/azure/sql-database/sql-database-manage-logins#using-fixed-and-custom-database-roles).
* The only way to change the server admin login is to recreate a new logical server. If there are already user databases created, you can [export](https://docs.microsoft.com/azure/sql-database/sql-database-export?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) the database as bacpac files and [import](https://docs.microsoft.com/azure/sql-database/sql-database-import?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) them from bacpac file in the new server.

## **Recommended Documents**

* [SQL pool Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)
* [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/)
* [Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017&viewFallbackFrom=sql-server-2017%2F?WT.mc_id=pid:13491:sid:32630405/)
* [TDE with Bring Your Own Key](https://docs.microsoft.com/azure/sql-database/transparent-data-encryption-byok-azure-sql?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630405/)
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Threat detection overview](https://docs.microsoft.com/azure/sql-database/sql-database-threat-detection?WT.mc_id=pid:13491:sid:32630457/)
* [Vulnerability assessment](https://docs.microsoft.com/azure/sql-database/sql-vulnerability-assessment?WT.mc_id=pid:13491:sid:32630461/)
* [Advanced Threat Protection Alerts](https://docs.microsoft.com/azure/sql-database/sql-database-threat-detection-overview#advanced-threat-protection-alerts)
* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)


