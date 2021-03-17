<properties
	pageTitle="Scale out your Azure Database for PostgreSQL Hyperscale server group"
	description="Scale out your Azure Database for PostgreSQL Hyperscale server group"
	infoBubbleText="Scale out your Azure Database for PostgreSQL Hyperscale server group"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="dbb4b343-7d38-4ce8-9580-b062d6adad12"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747926"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
    
# Scale out your Azure Database for PostgreSQL Hyperscale server group

## **Recommended Steps**

* You can add worker nodes to your Hyperscale Server Group [Scale out - Add worker nodes]( https://docs.microsoft.com/azure/azure-arc/data/scale-out-postgresql-hyperscale-server-group). Example: `azdata arc postgres server edit -n postgres01 -w 4`.
* Troubleshooting & FAQ
    * How can I monitor the state of the worker node being added? If the worker node is being added you will see Pending status for the server group using the command `azdata arc postgres server list`.
    * You can further check this from the PostgreSQL side `SELECT * FROM pg_dist_node;`
    * Will my database remain online during the Scale out operation? **Yes**. During this scale out operation the database remains fully online, and we can continue running queries.
    * Can I reduce the number of worker nodes? **No**. The preview release does not support scale back in. For example it is not yet possible to reduce the number of worker nodes. If you need to do so, you need to extract/backup the data, drop the server group, create a new server group with less worker nodes and then import the data.

## **Recommended Documents**

- [Show configuration of a server group](https://docs.microsoft.com/azure/azure-arc/data/show-configuration-postgresql-hyperscale-server-group)
- [Scale up/down (increase/decrease memory/vcore) a server group](https://docs.microsoft.com/azure/azure-arc/data/scale-up-down-postgresql-hyperscale-server-group-using-cli)
- [Scale out (add worker nodes)](https://docs.microsoft.com/azure/azure-arc/data/scale-out-postgresql-hyperscale-server-group)
- [Configure the Postgres database engine server parameters](https://docs.microsoft.com/azure/azure-arc/data/configure-server-parameters-postgresql-hyperscale)
- [Using Postgres extensions](https://docs.microsoft.com/azure/azure-arc/data/using-extensions-in-postgresql-hyperscale-server-group)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
- [Nodes and tables](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-nodes)
- [Determine application type](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-app-type)
- [Choose a distribution column](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-choose-distribution-column)
- [Table colocation](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-colocation)
- [Distribute and modify tables](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-modify-distributed-tables)
- [Design a multi-tenant database](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-hyperscale-multi-tenant)
- [Design a real-time analytics dashboard](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-hyperscale-realtime)