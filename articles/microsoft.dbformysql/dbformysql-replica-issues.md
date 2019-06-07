<properties
	pageTitle="General replication issues in Azure Database for MySQL"
	description="Replication issues"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ajlam"
    ms.author="andrela"
	displayOrder="55"
	selfHelpType="resource"
	supportTopicIds="32640065"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="mysqlissuereplication"
/>

# Issues with replication

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

**Issue:** Replica server is writable, but is normally read-only.

Look at the username field(username@severname) in your connection string. Confirm that the servername is the same as that of the replica.

## **Recommended Documents**

* [Overview on read replicas](https://docs.microsoft.com/azure/mysql/concepts-read-replicas)
