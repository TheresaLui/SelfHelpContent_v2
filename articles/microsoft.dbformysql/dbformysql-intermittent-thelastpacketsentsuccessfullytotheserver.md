<properties
  pagetitle="The last packet sent successfully to the server was X milliseconds ago."
  description="The last packet sent successfully to the server was X milliseconds ago."
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788526"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2088ca55-142e-48cc-968c-ae28e15219e8"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# The last packet sent successfully to the server was X milliseconds ago

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* Increase the value of the `Max_allowed_packet`, `Connect_timeout`, `net_write_timeout`, `net_read_timeout`, and  `wait_timeout` parameters, and then rerun your query.

* If this doesn't resolve the issue, check running processes by using the following command:

  `mysql>SHOW PROCESSLIST;`

  Look for SELECT and UPDATE statements that are in a locking state, and then kill those processes. For more information, see [KILL Statement](https://dev.mysql.com/doc/refman/5.7/en/kill.html).

## **Recommended documents**

* [Handle transient errors and connect efficiently to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-connectivity)
* [Troubleshoot connection issues to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
