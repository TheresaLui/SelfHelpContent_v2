<properties
  pagetitle="MySQL server has gone away"
  description="MySQL server has gone away"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse, jtoland"
  selfhelptype="Generic"
  supporttopicids="32788634"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="de264d87-84b3-41aa-b75c-2abbfe3d8ea9"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# MySQL server has gone away

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

This is a generic issue that occurs as a result of a client-side error.

**Seeing the "MySQL server has gone away" error constantly?**

  This can happen for one of the following reasons:

  1. **Old or outdated driver**: Microsoft recommends that you connect to Azure Database for MySQL using the latest client version for your application. Take a look at [the latest clients for MySQL from here](https://docs.microsoft.com/azure/mysql/how-to-connect-overview-single-server). MySQL documentation also lists connectors for using MySQL with applications and tools that are compatible with industry standards ODBC and JDBC. Any system that works with ODBC or JDBC can use Azure Database for MySQL. Find [MySQL connector downloads here](https://dev.mysql.com/downloads/connector/).

  2. **init_connect improperly configured**: Avoid using this parameter if you are seeing "MySQL server has gone away error". If necessary, ensure that you have the correct format for the argument as this parameter has different possibilities for the argument. That’s why it's not validated at the portal level and should be validated by the user. More information on [init_connect here](https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_init_connect).

     For example, setting the `parameter init­_connect` for the following values will results in the error "set tmp_table_size=512M; set max_heap_table_size=512M". To fix this issue, set the correct arguments as full-length data sizes for the parameter. This is mandatory here, and the correct syntax to use is:

     `set tmp_table_size=536870912; set max_heap_table_size=536870912`

  3. **Privilege issue**: A client application running on a different host doesn't have the necessary privileges to connect to the MySQL server from that host. Make sure that your application IP address has been added to an allow list in the Azure Database for MySQL firewall. For more information, see [Azure Database for MySQL server firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules).

**Seeing the "MySQL server has gone away" error intermittently?**

  1. **Server dropped an incorrect or too large packet**: Consider increasing the value of [max_allowed_packet](https://dev.mysql.com/doc/refman/8.0/en/packet-too-large.html) from the Azure Database for MySQL server parameter blade to avoid issues related to packet size.

  2. **Timeout**: For timeouts from the TCP/IP connection on the client side, consider mitigating the issue by tuning timeout-related server parameters such as `connect_timeout`, `innodb_lock_wait_timeout`, `interactive_timeout`, `lock_wait_timeout`, `max_execution_time`, `net_read_timeout`, `net_write_timeout`, and `wait_timeout`. For more information, see [Configure server parameters](https://docs.microsoft.com/azure/mysql/howto-server-parameters#configure-server-parameters).

  3. **DBA or Application terminated a running process**: If a DBA terminates the running thread with a KILL statement or a mysqladmin kill, you will encounter the "MySQL server has gone away" error.

  4. **Connection is already closed with the database server**: If a query is run after the connection to the server has closed, there's a logic error in the application that needs to be corrected. For more information, see [Transient errors](https://docs.microsoft.com/azure/mysql/concepts-connectivity#transient-errors).

   **Note**: For more information about how to address transient errors, see [Handling transient errors](https://docs.microsoft.com/azure/mysql/concepts-connectivity#handling-transient-errors)

## **Recommended documents**

* [Setting Azure MySQL parameters](https://docs.microsoft.com/azure/mysql/howto-server-parameters#setting-parameters-not-listed)
* [Azure Database for MySQL server has gone away](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-server-has-gone-away/ba-p/369138)
* [Troubleshoot connection issues to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
