<properties
    pageTitle="Security, Privacy and Compliance-Firewall Rules"
    description="Security, Privacy and Compliance-Firewall Rules"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635199"
    productPesIds="15818"
    displayOrder="81"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-securityprivacyandcompliance-firewallrules.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Troubleshooting Firewall rules

## **Recommended Steps**

* For setting up IP-based firewall rules, refer to this document [Azure SQL Data Warehouse IP firewall rules](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure?toc=/azure/sql-data-warehouse/toc.json&bc=/azure/sql-data-warehouse/breadcrumb/toc.json)
* For setting up virtual network private link, refer to this document [Private Link for Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-database/sql-database-private-endpoint-overview)
* For Polybase connectivity from Azure SQL Data Warehouse to Azure Storage under firewalls or virtual network, refer to [this](https://docs.microsoft.com/azure/sql-database/sql-database-private-endpoint-overview#connecting-from-an-azure-sql-data-warehouse-to-azure-storage-using-polybase) document
* For virtual network service endpoints, refer to [Use virtual network service endpoints for database servers](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview?toc=/azure/sql-data-warehouse/toc.json&bc=/azure/sql-data-warehouse/breadcrumb/toc.json)
* For details on Azure SQL Data Warehouse connectivity architecture, refer to [Azure SQL Connectivity Architecture](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture)
* For details on Network Security Groups and Azure Service tags, refer to this [Security groups](https://docs.microsoft.com/azure/virtual-network/security-overview#service-tags) document

## **Recommended Documents**

For other security capabilities, refer to these documents:

* [SQL Data Warehouse Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)
* [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/)
* [Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-2017&viewFallbackFrom=sql-server-2017/%3FWT.mc_id=pid:13491:sid:32630405/)
* [TDE with Bring Your Own Key](https://docs.microsoft.com/azure/sql-database/transparent-data-encryption-byok-azure-sql?view=sql-server-2017%3FWT.mc_id=pid:13491:sid:32630405/)
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32630410/)
* [Threat detection overview](https://docs.microsoft.com/azure/sql-database/sql-database-threat-detection?WT.mc_id=pid:13491:sid:32630457/)
* [Vulnerability assessment](https://docs.microsoft.com/azure/sql-database/sql-vulnerability-assessment?WT.mc_id=pid:13491:sid:32630461/)
* [Advanced Threat Protection](https://docs.microsoft.com/azure/sql-database/sql-advanced-threat-protection?WT.mc_id=pid:13491:sid:32630461/)
* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)
