<properties
    pageTitle="Install issues: AD sync service account"
    description="AD Sync or Service Account Issues"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629783"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public"
    />

# Install issues: AD sync service account

## **Recommended steps**
For an overview of the different accounts used by Azure AD Connect see this guide [Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions).

* The **ADSync service account** is used to run the synchronization service (ADSync) and access the SQL database.

* Many different types of account can be used for the ADSync service account ([Virtual Service Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#virtual-service-account), [Managed Service Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#group-managed-service-account), [User account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#user-account)). For a description of the different account types and the recommended options see this guide [ADSync Service Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions).

* The **Best Practice** in most scenarios is to allow the Azure AD Connect wizard to create the ADSync service account
    * If you are using Remote SQL then you need to provide your own account to be used as the ADSync service account.
    
    * During installation when using Remote SQL - a SQL login for the ADSync service account will be created and granted DBO permissions for the created database.

### **SQL Server considerations**

#### **Scale** 

* By default Azure AD Connect will use SQL Server 2010 Express LocalDB to store identity data [SQL Server used by Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites). 

* LocalDB has a 10GB size limit which enables you to manage approximately 100,000 objects. If you install using LocalDB and hit the size limit you can migrate to full SQL Server later as described here [Move LocalDB to SQL Server](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-move-db).

#### **Install options**

* You can install using an existing ADSync database. This guide explains why you may want to do this and how [Install using existing database](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-existing-database).

* You can install using SQL delegated administrator permissions [Install using SQL delegated administrator permissions](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-sql-delegation).

##### **Performance**

* Factors affecting SQL database performance are described here [SQL database factors](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-performance-factors).

##### **Troubleshooting**

* This article explains how to troubleshoot connectivity issues between Azure AD Connect and SQL Server [SQL Connectivity issues](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-tshoot-sql-connectivity).

## **Recommended documents**
* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)
* [ADSync service account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#adsync-service-account)
* [SQL Server used by Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites#sql-server-used-by-azure-ad-connect)
* [Troubleshoot SQL connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-tshoot-sql-connectivity)
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)