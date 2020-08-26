<properties
    pageTitle="Managing permissions in Azure Database for PostgreSQL servers"
    description="Managing permissions in Azure Database for PostgreSQL servers"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="480"
    selfHelpType="generic"
    supportTopicIds="32639989"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1f0fa8ae-1033-4d6a-afd6-ce1e02ce623a"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing permissions on in Azure Database for PostgreSQL servers

Each Azure Database for PostgreSQL server is created with a highly privileged admin role. User permissions for other users you create are managed through the PostgreSQL built-in user management capabilities. Please note that superuser access cannot be granted in the managed service.

## **Recommended Steps**

* For more information on how to manage users and roles in PostgreSQL, please refer to the [PostgreSQL documentation](https://www.postgresql.org/docs/current/user-manag.html) for the version you are using
* If you lose your admin account password, or you need to change the password for any reason follow the [reset password article](https://docs.microsoft.com/azure/postgresql/howto-create-manage-server-portal#update-admin-password) to manage your admin account

## **Recommended Documents**

* [Create users in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-create-users)
