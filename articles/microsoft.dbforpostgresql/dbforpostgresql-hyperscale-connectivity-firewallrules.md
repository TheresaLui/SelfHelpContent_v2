<properties
    pageTitle="Firewall rules on Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Firewall rules on Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource="serverGroups"
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-connectivity-firewallrules.md"
    selfHelpType="resource"
    supportTopicIds="32731219"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Firewall rule issue

## **Recommended Steps**
* The error *could not connect to server: Connection timed out. Is the server running on host and accepting TCP/IP connections on port 5432* typically indicates a firewall rule is needed. [Set up a firewall rule](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-manage-firewall-using-portal) to allow your client's IP address.
* If you've added a firewall rule and it does not seem to be taking effect: For temporary testing purposes only, set up a firewall rule using 0.0.0.0 as the starting IP address and using 255.255.255.255 as the ending IP address. That rule opens the server to all IP addresses. If the wide IP rule resolves your connectivity issue, double-check that you have the correct IP address for your client firewall rule. (Remember to delete the wide IP rule.)
* From your client network, ensure that port 5432 is open for outbound connections
* Make sure you are connecting to the database called `citus`
* Virtual networks (VNETs) are not currently available as a feature in Hyperscale (Citus)

## **Recommended Documents**
* [Manage firewall rules](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-manage-firewall-using-portal)
* [Troubleshoot connection issues](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-troubleshoot-common-connection-issues)