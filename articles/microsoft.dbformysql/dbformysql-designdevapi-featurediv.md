<properties
	pageTitle="Feature differences between MySQL PaaS and standalone MySQL"
	description="Feature differences between MySQL PaaS and standalone MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="12"
	selfHelpType="resource"
	supportTopicIds="32628387"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="2823993f-8c54-42f8-9f19-6fd99847ed61"
/>

# Feature differences between MySQL PaaS and standalone MySQL

Azure Database for MySQL uses the community edition of MySQL. Some limitations in functionality exist because Azure database for MySQL is a fully managed platform as a service. For example, we do not support the MyISAM storage engine because of the lack of ACID compliance. Super user access to the MySQL server is also not supported. For a list of current limitations, please check our [limits documentation](https://docs.microsoft.com/azure/mysql/concepts-limits).

## **Recommended Documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
