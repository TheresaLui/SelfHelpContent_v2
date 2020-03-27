<properties
	pageTitle="Outbound network connections from my app are failing"
	description="Outbound network connections from my app are failing"
	service="microsoft.web"
	resource="sites"
	authors="cts-shrahman,khaled-zayed"
    ms.author="shrahman, khzayed"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32730381"
	resourceTags=""
	productPesIds="14748,16333,16170"
	cloudEnvironments="public, MoonCake, Fairfax"
	articleId="60202514-c11c-471e-958e-36b34492ec2a"
	ownershipId="Compute_AppService"
/>

# Outbound network connections from my app are failing

## **Recommended Documents**

* [Outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)<br>
* [SNAT with App Service](https://4lowtherabbit.github.io/blogs/2019/10/SNAT/)<br>

**Node**<br>
By default, connections for NodeJS are not kept alive. Below are the popular databases and packages for connection pooling which contain examples for how to implement them. 

* [MySQL](https://github.com/mysqljs/mysql#pooling-connections)  
* [MongoDB](https://blog.mlab.com/2017/05/mongodb-connection-pooling-for-express-applications/)  
* [PostgreSQL](https://node-postgres.com/features/pooling)  
* [SQL Server](https://github.com/tediousjs/node-mssql#connection-pools)  

HTTP Keep-alive
* [agentkeepalive](https://www.npmjs.com/package/agentkeepalive)  
* [Node.js v13.9.0 Documentation](https://nodejs.org/api/http.html)  

**Java**<br>
Below are the popular libraries used for JDBC connection pooling which contain examples for how to implement them:

JDBC Connection Pooling
* [Tomcat 8](https://tomcat.apache.org/tomcat-8.0-doc/jdbc-pool.html)
* [C3p0](https://github.com/swaldman/c3p0)
* [Apache DBCP](https://commons.apache.org/proper/commons-dbcp/)

HTTP Connection Pooling
* [Apache Connection Management](https://hc.apache.org/httpcomponents-client-ga/tutorial/html/connmgmt.html)  
* [Class PoolingHttpClientConnectionManager](http://hc.apache.org/httpcomponents-client-ga/httpclient/apidocs/org/apache/http/impl/conn/PoolingHttpClientConnectionManager.html)

**PHP**<br>
Although PHP does not support connection pooling, you can try using persistent database connections to your backend server. 

* MySQL server
    - [MySQLi connections](https://www.php.net/manual/en/mysqli.quickstart.connections.php) for newer versions
    - [mysql_pconnect](https://www.php.net/manual/en/function.mysql-pconnect.php) for older versions of PHP<br>
* Other data Sources
    - [PHP Connection Management](https://www.php.net/manual/en/pdo.connections.php)

**Python** <br>
Below are some examples for connection pooling with Python. 
* [MySQL ](https://dev.mysql.com/doc/connector-python/en/connector-python-api-mysqlconnectionpool-constructor.html)
* [MongoDB](http://api.mongodb.com/python/2.1/api/pymongo/pool.html)
* [PostgreSQL](http://initd.org/psycopg/docs/pool.html)
* [SQL Server](https://docs.sqlalchemy.org/en/13/core/pooling.html) (NOTE: SQLAlchemy can be used with other databases besides MS SQL)
