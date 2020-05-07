<properties
    pageTitle="Availability and Connectivity in Azure Databases for MySQL"
    description="Established connection is dropped or terminated"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32640055"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="cf53cc8b-732f-4262-b101-f8eab4930254"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection issues to Azure Databases for MySQL

An established connection to an Azure Database for MySQL server can be terminated for multiple reasons, including client connection timeouts, changes of the server configuration, network failures, server restarts, and so on. Please work through the step below for a first level of troubleshooting your connection issue.

## **Recommended Steps**

* Try to reconnect to your server. If you are not able to reconnect, please switch to the problem subtype *Database is currently unavailable* to troubleshoot intermittent connection problems.
* Check the **Resource health** for your server to see if there were any reported events that could have caused the connection disruption.
* Check the **Activity log** for you database to see if there changes to the server that could have causes the connection drops.
* Validate the network connectivity between your client and database servers:

  * Use the *PING* command to confirm that name resolution successfully translates your server name to an IP address
  * Use the *telnet* to port 3306 using the IP address returned in the prior step. This will test whether there are any firewalls/routers blocking traffic to port 3306.

* Check your client logs if you are experiencing connection timeouts or query timeouts. If yes, please review your setting for the following server parameters: *connect_timeout*, *wait_timeout*, and *interactive_timeout*. Consult the MySQL documentation for current server version for more information.
* Constantly seeing "Server has gone away" error:

  * Review the [supported client driver list](https://docs.microsoft.com/azure/mysql/concepts-compatibility) and ensure you are using a driver that is supported
  * Review the **init_connect** server parameter is improperly configured with correct format
  * [Set up firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) to allow your client's IP address

* Intermittently seeing "Server has gone away" error:

  * Server dropped an incorrect or packet is too large. Please increase the value for **max_allowed_packet** from the Azure portal parameter pane to avoid issues due to the size of the packet.
  * You got a timeout from the TCP/IP connection on the client side. Please note that there are a number of parameters that can cause this timeout to happen. After the server waits for activity to happen, it will close the connection after the number of seconds specified by the corresponding parameter. Please increase **wait_timeout**, **net_read_timeout** and **net_write_timeout** parameters with proper values.

* Intermittently seeing "Out of memory" error:

  * Scale up to a higher [pricing tier](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers) to get more memory
  * Optimize the application query by avoiding to use the large join statement or large memory table
  * Review the *innodb_buffer_pool_pages_free* state by execute `show global status like 'innodb_buffer_pool_pages_free'`. If the value is not zero, consider reducing the **innodb_buffer_pool_size** from Azure portal server parameter to give more memory for ad-hoc query.

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
