<properties
	pageTitle="Managed Instance - Gateway under high CPU pressure"
	description="Managed Instance - Gateway under high CPU pressure"
	infoBubbleText="Gateway for Managed Instance was facing high CPU pressure. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="v-zlrade"
	authors="v-zlrade"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_GatewayUnderCpuPressure"
	selfHelpType="diagnostics"
	supportTopicIds="32637224,32637247"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-gateway-under-cpu-pressure"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Gateway under high CPU pressure

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> had degraded performance between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> due to high CPU pressure on the gateway for this instance.
<!--/issueDescription-->

Azure SQL MI provides two connection policy settings: proxy and redirect. In redirect mode, clients establish connection directly to the node hosting the instance, while in proxy mode, all connections are proxied via Azure SQL Database gateways. Redirect mode is strongly recommended in order to avoid performance degradation since in proxy mode all requests are proxied via gateway, which could lead to its high CPU pressure.


## **Recommended Steps**

* To enable normal operation of your instance, you should execute __az sql server conn-policy update__ command from  __Azure CLI__ in order to change your connection policy to redirect mode

	The following is a template of __az sql server conn-policy update__ command which you should execute after you modify parameters with appropriate values: 

```
az sql server conn-policy update --connection-type {Default, Proxy, Redirect}
                                 [--add]
                                 [--force-string]
                                 [--ids]
                                 [--remove]
                                 [--resource-group]
                                 [--server]
                                 [--set]
                                 [--subscription]
```

Keep in mind that `--connection-type` parameter is the only one which is required, and in this specific case it should be set to __Redirect__. Other [parameters are optional](https://docs.microsoft.com/cli/azure/sql/server/conn-policy). 

## **Recommended Documents**

* [Azure SQL Connectivity Architecture](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-architecture)
