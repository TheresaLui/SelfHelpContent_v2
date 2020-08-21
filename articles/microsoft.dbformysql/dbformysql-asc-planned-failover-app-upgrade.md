<properties
	pageTitle="Orcas MySQL Server planned failover app upgrade"
	description="RCA - Server planned failover app upgrade"
	infoBubbleText="Server planned failover detected. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformysql-planned-failover-app-upgrade"
	diagnosticScenario="OrcasMySQLPlannedFailOverAppUpgrade"
	selfHelpType="rca"
	resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect MySQL database server

<!--issueDescription-->
During our investigation regarding connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName-->, we determined that your MySQL server was restarted at <!--$StartTime-->StartTime<!--/$StartTime--> (UTC) causing connection attempts to fail. The server restarted because planned failover due to <!--$RCA-->RCA<!--/$RCA-->.

This App Upgrade deployment caused the server to fail over to other nodes in our infrastructure, which is the expected behavior. As failover switch secondary to primary, all current connections on primary will be dropped. Failover generally need to occur within 5-60 seconds for no impact to be seen but the deployment code is still being optimized and longer unavailability is possible. You can see if you server was impacted by a deployment by navigating to Resource Health for you server. Currently the 50th percentile of all servers world-wide fail over within 20 seconds. We are working aggressively to optimize the failover time further for all our customers. We suggest that our customers implement retry logic in their application for the database connectivity and consider connection pooling, thereby offering resiliency against such planned failover. 
<!--/issueDescription-->

## **Recommended Steps**

1. Errors like the above are transient in nature and your database server will come back online automatically. Please try to reconnect to your server to see if the server is back online.
2. As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Retry logic itself is aiming at handling such kind of transient faults in code when receiving some error and automatically reopen the connections. The simple logic is:Receiving error -> waiting for a very short period -> starting to connect again ->if failed again, increasing waiting time for a little bit longer and connect again. You will have control for this total wait time. We would suggest the total wait time is longer than 60 seconds. The benefits of retry-logic is that for transient outages within 60 seconds, it won’t throw exception for dropped connections. For end user, they won’t aware of the outages in general. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
