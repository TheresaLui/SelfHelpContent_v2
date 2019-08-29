<properties
  pageTitle="SQL Gateway Migration"
  description="SQL Gateway Migration"
  infoBubbleText="Found recent connectivity issue. See details on the right."
  service="microsoft.sql"
  resource="servers"
  authors="subbu-kandhaswamy, swbhartims"
  ms.author="subbuk, swbharti"
  displayOrder=""
  articleId="GatewayMigration_257E0082-CAC5-4934-812E-AC8DA79D9318"
  diagnosticScenario="crc_sqldb_connectivity"
  selfHelpType="diagnostics"
  supportTopicIds="32630429"
  resourceTags=""
  productPesIds="13491"
  cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC, server <!--$ServerName-->ServerName<!--/$ServerName--> was unreachable, and issue is related to recent migration of traffic connections to newer gateways in this region. This migration will change the public IP address that DNS resolves for database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName-->.

For further information, please refer to the documentation present in the link below.
<!--/issueDescription-->

## **Recommended Steps**

* Retry connecting to the database after a few minutes
* Add some type of retry logic to your application code

## **Recommended Documents**

* [Gateway Migration to new hardwares](https://docs.microsoft.com/azure/sql-database/sql-database-gateway-migration)
