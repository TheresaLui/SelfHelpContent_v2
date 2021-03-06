<properties
    pageTitle="Security in Azure Database for PostgreSQL"
    description="Security in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="470"
    selfHelpType="generic"
    supportTopicIds="32639965, 32780944"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="27d648a0-f2cc-4d25-8cf0-cc646ddd82dd"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Security in Azure Database for PostgreSQL

Azure Database for PostgreSQL comes with a rich set of security features, including server-level firewall rules, encryption for data at rest and in flight, Private Link, virtual network service endpoints, and Advanced Threat Protection. 

Advanced Threat Protection for Azure Database for PostgreSQL detects anomalous activities, which indicate unusual and potentially harmful attempts to access or exploit databases through integration with Azure Security Center.

## **Recommended Steps**

* Are you trying to enable Advanced Threat Protection for your server and can't find it in Azure portal?
    * Note that Advanced Threat Protection is not available in the Azure Government and Sovereign Cloud regions.

* Are you looking for Advanced Threat Protection for your Basic tier server?
    * Advanced Threat Protection require General Purpose or Memory Optimized servers.

## **Recommended Documents**

* [Advanced Threat Protection](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-threat-protection)
* [Firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)<br>
* [Configuring SSL](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security)<br>
* [VNet service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet)<br>
* [Private Link](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-private-link)
