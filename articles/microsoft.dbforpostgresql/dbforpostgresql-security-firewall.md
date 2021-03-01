<properties
    pageTitle="Managing firewall rules for Azure Database for PostgreSQL"
    description="Managing firewall rules for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="460"
    selfHelpType="generic"
    supportTopicIds="32639981, 32780946"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3b2cdd35-8f48-40b3-88de-ea7c22c0bdb7"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing firewall rules for Azure Database for PostgreSQL

Server-level firewall rules are used to manage access via public IP to your Azure Database for PostgreSQL - Single server. You can define specific public IP address or a range of public IP addresses that would be able to connect to your PostgreSQL server. These firewall rules can be managed through the Azure [portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).

Most users are able to resolve their firewall issue using the steps below.

## **Recommended steps**

* Did you set 'Deny public network access' to 'Yes' on 'Connection security' page in Azure portal?
  * When 'Deny public network access' is set to 'Yes', the firewall rules you may have configured in your Azure Database for PostgreSQL - Single server are disabled. If you need to access your Postgres server via its public IP make sure 'Deny public network access' is set to 'No'.
* Are you trying to connect to your server *too soon* after setting new firewall rules?
  * It may take up to **five-minutes** for changes to the Azure Database for PostgreSQL - Single server firewall configuration to take effect. Confirm your rule was added and re-try to connect after at least five minutes.

* Are your errors related to firewall rules and connectivity?
  * Make sure you specified *user name* in the right format: username&your_postgres_server_name; e.g. user@server1
  * Make sure your security credentials are valid in case you are seeing the *authentication errors*
  * Make sure you specified right *database name* 

* Are you getting errors connecting to your server while firewall rules seem to be set correctly?
  * Add **temporarily** a firewall rule on your Azure Database for PostgreSQL - Single server for all IP addresses (0.0.0.0 - 255.255.255.255).
  * Wait for five minutes to ensure that the rule became effective. 
  * Try to connect again. 
    * If you **can connect**, you have everything set correctly but the actual public IP address used by your client to connect to your Postgres server was not included in the firewall rules. 
      * Remove temporary 0.0.0.0 - 255.255.255.255 firewall rule.
      * Double check the actual public IP or range of public IP addresses for your client.
      * Add it to the firewall rules on your Postgres server.
    * If you still **can't connect** with this temporary firewall rule, you need to troubleshoot connectivity on your client or in your network  
      * Validate that the firewall *on the client* or in your network allows outbound traffic on the required port (5432) and to [the public IPs used by Azure Database for PostgreSQL - Single server](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture#azure-database-for-postgresql-gateway-ip-addresses). 
      * If your client does not have a static public IP address, this *dynamic public IP address* might not be covered by the firewall rule. Make sure that you're including the full range of your outgoing public IPs in the Azure Database for PostgreSQL firewall rules.
  * **Do not forget** to remove temporary 0.0.0.0 - 255.255.255.255 firewall rule from your server once you finish troubleshooting as it allows connection from any host on the Internet.
 
* Are you having trouble using **Azure CLI**?
  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az postgres server firewall-rule** with valid values. Review the [Azure CLI PostgreSQL firewall rule](https://docs.microsoft.com/cli/azure/postgres/server/firewall-rule?view=azure-cli-latest) documentation for valid parameters.

* You can't connect but server's IP appears to be public and you can ping or connect to it using telnet?

  * Connections to the Azure Database for PostgreSQL - Single server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules.

## **Recommended Documents**

* [Managing firewall rules in the portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal)<br>
* [Managing firewall rules using CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli)<br>
* [Firewall rule concepts in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)<br>
* [Azure Database for PostgreSQL CLI reference documentation](https://docs.microsoft.com/cli/azure/postgres?view=azure-cli-latest)<br>
* [Azure Database for PostgreSQL REST API reference documentation](https://docs.microsoft.com/rest/api/postgresql/)
