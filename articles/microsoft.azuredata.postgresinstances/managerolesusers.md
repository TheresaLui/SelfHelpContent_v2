<properties
	pageTitle="Manage Roles and Users"
	description="Manage Roles and Users"
	infoBubbleText="Manage Roles and Users"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="10c1a35b-40bc-4977-a37c-229845376b48"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747933"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
    
# Configure security for your Azure Arc enabled PostgreSQL Hyperscale server group
    
## **Recommended Steps**

* If your issue is about changing the password of the Postgres administrative user follow the steps [here](https://docs.microsoft.com/azure/azure-arc/data/configure-security-postgres-hyperscale#change-the-password-of-the-postgres-administrative-user)
* If your issue is about creating user and roles
	* For Postgres in general, read: [Create role](https://www.postgresql.org/docs/12/sql-createrole.html) and [Create user](https://www.postgresql.org/docs/12/sql-createuser.html).
	* For Azure Arc enabled Postgres Hyperscale you can use the standard Postgres way to create users or roles. However, if you do so, these artifacts will only be available on the coordinator role. During preview, these users/roles will not yet be able to access data that is distributed outside the Coordinator node and on the Worker nodes of your server group. The reason is that in preview, the user definition is not replicated to the Worker nodes.
	
## **Recommended Documents**

- [Roles](https://www.postgresql.org/docs/11/user-manag.html)
- [Configure security in Azure Arc enabled PostgreSQL Hyperscale](https://docs.microsoft.com/azure/azure-arc/data/configure-security-postgres-hyperscale)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
