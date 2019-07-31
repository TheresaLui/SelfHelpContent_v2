<properties
	pageTitle="Security in Azure Database for PostgreSQL"
	description="Security in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="22"
	selfHelpType="resource"
	supportTopicIds="32639965, 32639967, 32639981, 32640029"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="MoonCake"
	articleId="d71ecddf-9ffc-4968-8e51-d214ed7d9569"
/>

# Security in Azure Database for PostgreSQL

Azure Database for PostgreSQL comes with a rich set of security features including server level firewall rules, encryption for data at rest and in flight, VNet service endpoints, and Advanced Threat Protection. Currently we do not support encryption at rest with customer keys and injecting a server directly into a VNet with a dedicated private IP.

## **Recommended Documents**

* [Firewall rules](https://docs.azure.cn/postgresql/concepts-firewall-rules)
* [Configuring SSL](https://docs.azure.cn/postgresql/concepts-ssl-connection-security)
* [VNet service endpoints](https://docs.azure.cn/postgresql/concepts-data-access-and-security-vnet)
