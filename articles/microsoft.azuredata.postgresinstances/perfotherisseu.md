<properties
	pageTitle="Data Modelling & Sharding , General issues"
	description="General issues Data Modelling & Sharding"
	infoBubbleText="General issues ,Data Modelling & Sharding"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="3b0339b6-7ee5-4364-a350-8e44ad6a5d64"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32745075"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
# PostgreSQL Hyperscale concepts

## **Recommended Steps**

Azure Database for PostgreSQL Hyperscale (Citus) is the same technology that is hosted as a service in Azure (Platform As A Service also known as PAAS) instead of being offered as part of Azure Arc enabled Data Services. The concepts and How-to guides for distributing your data across multiple Postgres Hyperscale nodes however holds good for Azure Arc Enabled Data Services too.

### PostgreSQL Hyperscale concepts

* [Nodes and tables](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-nodes)
* [Determine application type](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-app-type)
* [Choose a distribution column](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-choose-distribution-column)
* [Table colocation](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-colocation)
* [Distribute and modify tables](https://docs.microsoft.com/azure/postgresql/howto-hyperscale-modify-distributed-tables)
* [Design a multi-tenant database](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-hyperscale-multi-tenant)
* [Design a real-time analytics dashboard](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-hyperscale-realtime)

## **Recommended Documents**

- [Useful Diagnostic Queries Citus](http://docs.citusdata.com/v9.4/admin_guide/diagnostic_queries.html) 
- [Tuning your PostgreSQL Server](https://wiki.postgresql.org/wiki/Tuning_Your_PostgreSQL_Server) 
- [Using Postgres extensions](https://docs.microsoft.com/azure/azure-arc/data/using-extensions-in-postgresql-hyperscale-server-group)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
- [Kubernetes - Troubleshooting pods](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-pod-replication-controller/)
- [Kubernetes Debug Running Pod](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-running-pod/)
- [Options for Highly Available topology](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/ha-topology/)
- [Creating Highly Available clusters with kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/high-availability/)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
