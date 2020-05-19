<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="haz"
	ms.author="haz"
	displayOrder="100"
	articleId="dbformariadb-asc-18456-2-unknown"
	diagnosticScenario="OrcasMariaDBBackendErrorUnKnownReasons"
	selfHelpType="rca"
	supportTopicIds="32640117,32640118,32640120"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect MariaDB database server

<!--issueDescription-->
During our investigation regarding connection issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we determined that the server was restarted between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC), causing <!--$Count-->Count<!--/$Count--> connection attempts to fail. We have forwarded the issue to the MariaDB engineering team for further investigation. We will reach back out to you with more information shortly.
<!--/issueDescription-->

## **Recommended Steps**

As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mariadb/concepts-connectivity) for more details.

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums)
