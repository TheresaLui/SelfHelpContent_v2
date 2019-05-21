<properties
	pageTitle="General replication issues in Azure Database for PostgreSQL"
	description="Replication issues"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="rachel-msft"
    ms.author="raagyema"
	displayOrder="55"
	selfHelpType="resource"
	supportTopicIds="32639992"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="postgresgeneralreplication"
/>

# Issues with replication

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

**Issue:** Replica server is writable, or has some other property expected only on master.

1. Connect to your replica server and run the following query: `SELECT pg_is_in_recovery();`. If this returns false, you are not connected to a replica server. Look at the username field(username@severname) in your connection string. Confirm that the servername is the same as that of the replica.

**Issue:** Queries on the replica fail with error message "Canceling statement due to conflict with recovery. User query might have needed to see row versions that must be removed." 

Consider setting the parameter `hot_standby_feedback` to `ON`. To learn about this parameter, see [the PostgreSQL documentation](https://www.postgresql.org/docs/10/runtime-config-replication.html). [Learn how to set PostgreSQL server parameters in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal).


**Issue:** Queries on the replica fail with error message "Canceling statement due to conflict with recovery. User was holding shared buffer pin for too long."

Consider setting the parameters `max_standby_archive_delay` and `max_standby_streaming_delay` to a larger value. For an explanation of these parameters see [the PostgreSQL documentation](https://www.postgresql.org/docs/10/runtime-config-replication.html). [Learn how to set PostgreSQL server parameters in Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal). 


## **Recommended Documents**

* [Overview on read replicas](https://docs.microsoft.com/azure/postgresql/concepts-read-replicas)
