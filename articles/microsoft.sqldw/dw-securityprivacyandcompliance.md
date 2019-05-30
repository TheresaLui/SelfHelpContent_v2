<properties
	pageTitle="Security, Privacy and Compliance"
	description="Security, Privacy and Compliance"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635183, 32635184, 32635185, 32635187, 32635191, 32635199, 32635213, 32635221, 32635222, 32635233"
	productPesIds="15818"
	displayOrder="80"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-securityprivacyandcompliance.md"
	cloudEnvironments="public"
/>
# Security, Privacy and Compliance

## **Recommended Steps**
The following details explain how to set up and update common access and permissions rules in Azure SQL Data Warehouse.

* If you're looking to change the administrator password for a logical SQL Server, you can simply click "Reset Password" at the top of the SQL Server resource blade<br>
* [Configure SQL Azure firewall rules](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-get-started-provision/#create-a-new-azure-sql-server-level-firewall) for the IP addresses that are authorized to access this data warehouse<br>
* To set-up and connect to SQL Data Warehouse using [Azure Active Directory](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-authentication/) authentication<br>
* [Secure your SQL Data Warehouse](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)

### What access control can be done at the server level

* Roles cannot be made at the [server level](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-server-role?view=sql-server-2017&viewFallbackFrom=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/), they must be made at the database level
* The only way to change the server admin login is to recreate a new logical server. If there are already user databases created, you can [export](https://docs.microsoft.com/azure/sql-database/sql-database-export?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) the database as bacpac files and [import](https://docs.microsoft.com/azure/sql-database/sql-database-import?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) them from bacpac file in the new server.

## **Recommended Documents**

* [SQL Data Warehouse Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)<br>
* [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/)<br>
* [Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017&viewFallbackFrom=sql-server-2017%2F?WT.mc_id=pid:13491:sid:32630405/)<br>
* [TDE with Bring Your Own Key](https://docs.microsoft.com/azure/sql-database/transparent-data-encryption-byok-azure-sql?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630405/)<br>
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)<br>
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)<br>
* [Threat detection overview](https://docs.microsoft.com/azure/sql-database/sql-database-threat-detection?WT.mc_id=pid:13491:sid:32630457/)<br>
* [Vulnerability assessment](https://docs.microsoft.com/azure/sql-database/sql-vulnerability-assessment?WT.mc_id=pid:13491:sid:32630461/)<br>
* [Advanced Threat Protection](https://docs.microsoft.com/azure/sql-database/sql-advanced-threat-protection?WT.mc_id=pid:13491:sid:32630461/)
* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)