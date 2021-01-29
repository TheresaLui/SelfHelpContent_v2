<properties
    pageTitle="Creating and managing cluster/server group in Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Creating and managing cluster/server group in Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource=""
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-crud-servergroup.md"
    selfHelpType="generic"
    supportTopicIds="32731223"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Creating and managing server group

## **Recommended Steps**

**Roles (Users) and Databases**
* The `citus` role (user) is the most privileged role available to you. The citus role has [various permissions](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-create-users#the-server-admin-account) and two notable restrictions:
   * Cannot create databases
   * Cannot create roles
* To create and manage additional roles in Hyperscale (Citus), review [the roles how-to](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-create-users#how-to-create-additional-user-roles)
* You cannot delete the `citus` role
* You cannot create additional databases. You can create multiple schemas within the `citus` database.

## **Recommended Documents**
* [How to create a Hyperscale (Citus) server group](https://docs.microsoft.com/azure/postgresql/quickstart-create-hyperscale-portal)
* [Roles in Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-create-users)
