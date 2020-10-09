<properties
	pageTitle="Error Connecting to PostgreSQL Hyperscale Server Group"
	description="Error Connecting to PostgreSQL Hyperscale Server Group"
	infoBubbleText="Error Connecting to PostgreSQL Hyperscale Server Group"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="a998dee4-4631-4757-9608-d4cdbae5f8b2"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747904"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
	
# Error Connecting to PostgreSQL Hyperscale Server Group

Most users are able to resolve their connectivity issues using the steps below.

## **Recommended Steps** 

* You can get your connection endpoints by querying `azdata arc postgres server endpoint list -n servergroupname`.You can then use these endpoints to form your connection strings and connect with your client tools or applications.
* Access the Grafana and Kibana dashboards from your browser
	* Note:If you are using an Azure virtual machine to test, then the endpoint IP address will not show the public IP address. To locate the public IP address, use the steps [Special Note about Azure VM Deployments](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group#special-note-about-azure-virtual-machine-deployments).
	* [Get connection endpoints and query](https://docs.microsoft.com/azure/azure-arc/data/get-connection-endpoints-and-connection-strings-postgres-hyperscale)
* [List server groups](https://docs.microsoft.com/azure/azure-arc/data/list-server-groups-postgres-hyperscale) 
* [Connect with Azure Data Studio](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group#connect-with-azure-data-studio)
* [Connect with PSQL](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group#connect-with-psql)

## **Recommended Documents**

- [Configure security for PostgreSQL Hyperscale Server groups](https://docs.microsoft.com/azure/azure-arc/data/configure-security-postgres-hyperscale)
- [Login to Azure Arc Data Controller](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group#login-to-the-azure-arc-data-controller) 
- [Retrieve the user name and password to connect to the Arc Data Controller](https://docs.microsoft.com/azure/azure-arc/data/retrieve-the-username-password-for-data-controller)
- [Preliminary Steps for Open Shift Users only](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group#preliminary-and-temporary-step-for-openshift-users-only) 
- [Troubleshooting Hyperscale Server Groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Access Grafana & Kibana Dashboards](https://docs.microsoft.com/azure/azure-arc/data/monitor-grafana-kibana)