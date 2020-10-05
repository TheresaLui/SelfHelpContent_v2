<properties
	pageTitle="Modify Hyperscale Server Group"
	description="Modify Hyperscale Server Group"
	infoBubbleText="Modify Hyperscale Server Group"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="6713c21e-3851-4ba7-bbf4-a1e9ecfa17c51"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747911"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
    
# Modify Hyperscale Server Group

The below steps explains how to display the configuration of your server group(s). There are also times when you may need to change the characteristics or the definition of a server group.

## **Recommended Steps**
Most users are able to get their answers to the questions from the below steps:

* View the current definition of the Server Group: `azdata arc postgres server show -n servergroupname`
* For details about which parameters to change: `azdata arc postgres server edit --help`
* [Show configuration of a server group](https://docs.microsoft.com/azure/azure-arc/data/show-configuration-postgresql-hyperscale-server-group)
* [Scale up/down (increase/decrease memory/vcore) a server group](https://docs.microsoft.com/azure/azure-arc/data/scale-up-down-postgresql-hyperscale-server-group-using-cli)
* [Scale out (add worker nodes)](https://docs.microsoft.com/azure/azure-arc/data/scale-out-postgresql-hyperscale-server-group)
* [Configure the Postgres database engine server parameters](https://docs.microsoft.com/azure/azure-arc/data/configure-server-parameters-postgresql-hyperscale)

## **Recommended Documents**

- [Using Postgres extensions](https://docs.microsoft.com/azure/azure-arc/data/using-extensions-in-postgresql-hyperscale-server-group)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
- [Storage Configuration](https://github.com/microsoft/Azure-data-services-on-Azure-Arc/blob/master/docs/storage-configuration.md)
