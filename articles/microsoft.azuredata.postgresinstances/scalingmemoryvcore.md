<properties
	pageTitle="Scale memory , vcore Azure Database for PostgreSQL Hyperscale server group"
	description="Scale memory, vcore Azure Database for PostgreSQL Hyperscale server group"
	infoBubbleText="Scale memory, vcore Azure Database for PostgreSQL Hyperscale server group"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="f902f865-86f2-45b0-b817-99b9d9df8fb4"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747928"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
    
# Scale up and down an Azure Database for PostgreSQL Hyperscale server group using CLI (azdata)

Most users are able to Scale up or down the number of vCore &  memory that each of the coordinator or the worker nodes use using the below steps.

## **Recommended Steps**

* The vCore and memory settings apply per nodes, coordinator node and worker nodes. At this point we do not support setting the definitions of the coordinator node and the worker nodes separately. This is an element on the road map. Example: `azdata arc postgres server edit -n <name of your server group> --cores-request 2  --cores-limit 4  --memory-request 512Mi  --memory-limit 1024Mi`.
* The command executes successfully when it shows
	* `<name of your server group> is Ready`
	* Run again the command to display the definition of the server group and verify it is set as you desire `azdata arc postgres server show -n <the name of your server group>`
*  You can read more information on how to [Scale up/down (increase/decrease memory/vcore) a server group](https://docs.microsoft.com/azure/azure-arc/data/scale-up-down-postgresql-hyperscale-server-group-using-cli) .

## **Recommended Documents**

- [Show configuration of a server group](https://docs.microsoft.com/azure/azure-arc/data/show-configuration-postgresql-hyperscale-server-group)
- [Scale out (add worker nodes)](https://docs.microsoft.com/azure/azure-arc/data/scale-out-postgresql-hyperscale-server-group)
- [Configure the Postgres database engine server parameters](https://docs.microsoft.com/azure/azure-arc/data/configure-server-parameters-postgresql-hyperscale)
- [Using Postgres extensions](https://docs.microsoft.com/azure/azure-arc/data/using-extensions-in-postgresql-hyperscale-server-group)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
