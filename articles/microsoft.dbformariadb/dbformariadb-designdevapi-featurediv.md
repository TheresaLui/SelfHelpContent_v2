<properties
	pageTitle="Feature differences between MariaDB PaaS and standalone MariaDB"
	description="Feature differences between MariaDB PaaS and standalone MariaDB"
	service="microsoft.dbformariadb"
	resource="servers"
	authors="ajlam"
    ms.author="andrela"
	displayOrder="12"
	selfHelpType="resource"
	supportTopicIds="32640127"
	resourceTags="servers, databases"
	productPesIds="16617"
	cloudEnvironments="public"
	articleId="mariadbfeaturediff"
/>

# Feature differences between MariaDB PaaS and standalone MariaDB

Azure Database for MariaDB uses the community edition of MariaDB. Some limitations in functionality exist because Azure database for MariaDB is a fully managed platform as a service. For example, we do not support the MyISAM storage engine because of the lack of ACID compliance. Super user access to the MariaDB server is also not supported. For a list of current limitations, please check our [limits documentation](https://docs.microsoft.com/azure/mariadb/concepts-limits).

## **Recommended Documents**

* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
