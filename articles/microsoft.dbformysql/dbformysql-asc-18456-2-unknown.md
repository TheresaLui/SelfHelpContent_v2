<properties
	pageTitle="Server unavailable"
	description="RCA - Server unavailable"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="janeng"
	displayOrder="100"
	articleId="dbformysql-asc-18456-2-unknown"
	diagnosticScenario="OrcasMySQLBackendErrorUnKnownReasons"
	selfHelpType="rca"
	supportTopicIds="32628367"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public"
/>
# Can't connect MySQL database server

<!--issueDescription-->
Thank you for contacting Microsoft support about your connection issues to your MySQL server <!--$ServerName-->ServerName<!--/$ServerName-->. During our initial investigation we determined that the server was restarted between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->, causing <!--$Count-->Count<!--/$Count--> connection attempts to fail. We have forwarded the issue to the MySQL engineering team for further investigation. We will reach back out to you with more information shortly.
<!--/issueDescription-->

## **Recommended steps**

As the service cannot entirely prevent transient connection failures like the one above from happening, we encourage all customers to implement retry logic. Please refer to our [documentation](https://docs.microsoft.com/azure/mysql/concepts-connectivity) for more details.

## **Recommended documents**

[Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)

[MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=AzureDatabaseforMySQL)