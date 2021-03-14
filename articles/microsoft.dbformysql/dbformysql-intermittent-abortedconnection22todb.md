<properties
  pagetitle="ERROR 1184 (08S01): Aborted connection 22 to db"
  description="ERROR 1184 (08S01): Aborted connection 22 to db"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788512"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="e7044e0a-cf6e-4c4a-bc6c-d7023e0c2bb4"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Azure Database for MySQL ERROR 1184 (08S01): Aborted connection 22 to db

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

ERROR 1184 (08S01): "Aborted connection 22 to db" occurs after a successful login, but before executing any command when the session is established. If you receive this error message, you've set an incorrect value for the `init_connect server` parameter, which caused session initialization to fail.

In addition, some server parameters, such as `require_secure_transport`, are not supported at the session level. As a result, trying to change the values of these parameters using `init_connect` can result in Error 1184 while connecting to the MySQL server, as shown below:

  ``mysql> show databases; ERROR 2006 (HY000): MySQL server has gone away No connection. Trying to reconnect... Connection id: 64897 Current database: *** NONE *** ERROR 1184 (08S01): Aborted connection 22 to db: 'db-name' user: 'user' host: 'hostIP' (init_connect command failed)``

### Resolution

To resolve this issue, in the Azure portal, on the **Server parameters** tab, reset the value of the `init_connect` parameter, and then use only the values supported by the `init_connect` parameter.

## **Recommended documents**

* [ERROR 1184 (08S01): Aborted connection 22 to db](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-errors#error-1184-08s01-aborted-connection-22-to-db-db-name-user-user-host-hostip-init_connect-command-failed)
