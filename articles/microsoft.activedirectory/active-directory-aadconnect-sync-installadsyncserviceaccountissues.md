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
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="77af65ea-b6be-4956-a3cf-dd2c16ca7075"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Install issues: AD sync service account

## **Recommended Steps**

* For an overview of the different accounts used by Azure AD Connect, see the [Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions) guide
* The **ADSync service account** is used to run the synchronization service (ADSync) and access the SQL database
* Many different types of accounts can be used for the ADSync service account ([Virtual Service Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#virtual-service-account), [Managed Service Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#group-managed-service-account), and [User account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#user-account)). For a description of the different account types and the recommended options, see the [ADSync Service Account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions) guide.
* The **Best Practice** in most scenarios is to allow the Azure AD Connect wizard to create the ADSync service account
    * If you are using Remote SQL then you need to provide your own account to be used as the ADSync service account
    * During installation when using Remote SQL, an SQL login for the ADSync service account will be created and granted DBO permissions for the created database

### **SQL Server considerations**

#### **Scale** 

* By default Azure AD Connect will use [SQL Server 2010 Express LocalDB](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites) to store identity data 
* LocalDB has a 10GB size limit which enables you to manage approximately 100,000 objects. If you install using LocalDB and hit the size limit you can [migrate to full SQL Server](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-move-db)

#### **Install options**

* You can install using an [existing ADSync database](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-existing-database)
* You can install using [SQL delegated administrator permissions](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-sql-delegation)

##### **Performance**

* Review factors affecting [SQL database performance](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-performance-factors)

##### **Troubleshooting**

* [Azure AD Connect and SQL Server Connectivity issues](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-tshoot-sql-connectivity)

## **Recommended Documents**

* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)
* [ADSync service account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions#adsync-service-account)
* [SQL Server used by Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites#sql-server-used-by-azure-ad-connect)
* [Troubleshoot SQL connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-tshoot-sql-connectivity)
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)
