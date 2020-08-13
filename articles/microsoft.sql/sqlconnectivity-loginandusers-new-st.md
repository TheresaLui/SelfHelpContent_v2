<properties
    pageTitle="How to questions: Login and Users"
    description="How to questions: Login and Users"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745433"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="0414DD20-F31A-400E-81A1-04EC346296AE"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Login and Users - How to Configure and use

### **Authentication, Logins and Users**

Azure SQL Database supports two authentication methods, **SQL Authentication** and **Azure Active Directory Authentication**.

In **SQL authentication**  users will submit a user account name and associated password to establish a connection. This password is stored in the master database for user accounts linked to a login or stored in the database containing the user accounts not linked to a login.

In **Azure Active Directory Authentication** method, users submit a user account name and requests that the service use the credential information stored in Azure Active Directory (Azure AD).    

**Logins and users**

* A user account in a database can be associated with a login that is stored in the master database or can be a user name that is stored in an individual database
- A *Login* is an individual account in the master database, to which a user account in one or more databases can be linked. With a login, the credential information for the user account is stored with the login.
- A *User account* is an individual account in any database that may be, but does not have to be, linked to a login. With a user account that is not linked to a login, the credential information is stored with the user account.
* **Server Admin** - When you first deploy Azure SQL, you specify an admin login and an associated password for that login. This administrative account is called Server admin.
* **Azure AD Admin** - Remember, every server (which hosts Azure SQL Database) starts with a single server administrator account (**Server Admin**) that is the administrator of the entire server. Azure AD admin will be created as the second administrator account as an Azure AD account. And this principal (AAD Admin) will be  created as a contained database user in the master database of the server.

## **Recommended Documents**

Please refer the following documents for additional information on Creating Logins & Users, Troubleshooting Login issues:

- [Configuring and Managing Login and Users](https://docs.microsoft.com/azure/azure-sql/database/logins-create-manage?WT.mc_id=pid:13491:sid:32745433/)
- [Active Directory Authentication for Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-overview?WT.mc_id=pid:13491:sid:32745433/)
- [Troubleshooting Login issues for Azure Active directory Users](https://techcommunity.microsoft.com/t5/azure-sql-database/troubleshooting-problems-related-to-azure-ad-authentication-with/ba-p/1062991?WT.mc_id=pid:13491:sid:32745433/)
