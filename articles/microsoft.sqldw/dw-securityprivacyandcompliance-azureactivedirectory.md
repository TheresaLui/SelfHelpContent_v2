<properties
    pageTitle="Security, Privacy and Compliance-AzureActiveDirectory"
    description="Security, Privacy and Compliance-AzureActiveDirectory"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635187"
    productPesIds="15818"
    displayOrder="81"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-securityprivacyandcompliance-azureactivedirectory.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Troubleshooting Azure Active Directory Authentication

## **Recommended Steps**

Azure Active Directory Authentication

* Set up and connect to SQL Data Warehouse using [Azure Active Directory](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication?toc=/azure/sql-data-warehouse/toc.json) authentication
* With Azure AD authentication, you can centrally manage the identities of database users and other Microsoft services in one central location. Benefits include the following:

  * It provides an alternative to SQL Server authentication
  * Helps stop the proliferation of user identities across database servers
  * Allows password rotation in a single place
  * Customers can manage database permissions using external (Azure AD) groups
  * It can eliminate storing passwords by enabling integrated Windows authentication and other forms of authentication supported by Azure Active Directory
  * Azure AD authentication uses contained database users to authenticate identities at the database level
  * Azure AD supports token-based authentication for applications connecting to SQL Database
  * Azure AD authentication supports ADFS (domain federation) or native user/password authentication for a local Azure Active Directory without domain synchronization
  * Azure AD supports connections from SQL Server Management Studio that use Active Directory Universal Authentication, which includes Multi-Factor Authentication (MFA). MFA includes strong authentication with a range of easy verification options — phone call, text message, smart cards with pin, or mobile app notification. For more information, see [SSMS support for Azure AD MFA with SQL Database and SQL Data Warehouse](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication).
  * Azure AD supports similar connections from SQL Server Data Tools (SSDT) that use Active Directory Interactive Authentication. For more information, see [Azure Active Directory support in SQL Server Data Tools (SSDT)](https://docs.microsoft.com/sql/ssdt/azure-active-directory).

## **Recommended Documents**

* [SQL Data Warehouse Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)
* [Monitor AD FS using Azure AD Connect Health](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-adfs)
* [AD FS Troubleshooting - Event and Logging](https://docs.microsoft.com/windows-server/identity/ad-fs/troubleshooting/ad-fs-tshoot-logging)
