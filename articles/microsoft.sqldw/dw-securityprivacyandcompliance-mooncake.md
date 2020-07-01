<properties
	pageTitle="Security, Privacy and Compliance"
	description="Security, Privacy and Compliance"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	supportTopicIds=""
	productPesIds=""
	displayOrder="19"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-securityprivacyandcompliance-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>
# Security, Privacy and Compliance

## **Recommended Steps**
The following details explain how to set up and update common access and permissions rules in Azure SQL Data Warehouse.

* If you're looking to change the administrator password for a logical SQL Server, you can simply click "Reset Password" at the top of the SQL Server resource blade
* [Configure SQL Azure firewall rules](https://docs.azure.cn/sql-data-warehouse/create-data-warehouse-portal#create-a-new-azure-sql-server-level-firewall) for the IP addresses that are authorized to access this data warehouse
* To set-up and connect to SQL Data Warehouse using [Azure Active Directory](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-authentication) authentication
* [Secure your SQL Data Warehouse](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-overview-manage-security)

### What access control can be done at the server level

* Roles cannot be made at the [server level](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-server-role?view=sql-server-2017&viewFallbackFrom=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/), they must be made at the database level
* The only way to change the server admin login is to recreate a new logical server. If there are already user databases created, you can [export](https://docs.azure.cn/sql-database/sql-database-export?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) the database as bacpac files and [import](https://docs.azure.cn/sql-database/sql-database-import?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) them from bacpac file in the new server.

## **Recommended Documents**

* [SQL Data Warehouse Security Overview](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-overview-manage-security)
* [Auditing - servers, pools, and databases](https://docs.azure.cn/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/)
* [Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017&viewFallbackFrom=sql-server-2017%2F?WT.mc_id=pid:13491:sid:32630405/)
* [TDE with Bring Your Own Key](https://docs.azure.cn/sql-database/transparent-data-encryption-byok-azure-sql?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630405/)
* [Configure Azure AD authentication](https://docs.azure.cn/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Configure multi-factor authentication for Azure AD](https://docs.azure.cn/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Threat detection overview](https://docs.azure.cn/sql-database/sql-database-threat-detection?WT.mc_id=pid:13491:sid:32630457/)
* [Vulnerability assessment](https://docs.azure.cn/sql-database/sql-vulnerability-assessment?WT.mc_id=pid:13491:sid:32630461/)
* [Advanced Threat Protection](https://docs.azure.cn/sql-database/sql-database-advanced-data-security?WT.mc_id=pid%3A13491%3Asid%3A32630461%2F)
