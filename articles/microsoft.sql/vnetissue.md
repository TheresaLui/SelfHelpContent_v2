<properties
	pageTitle="Database Connectivity issue due VNet Rules"
	description="VNetRuleIssue"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	displayOrder=""
	articleId="vNetIssue_96EAE137-BB69-4B9E-863A-72D23CBFE32F"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="32589555"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Connections for database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> originating from Subnet: <!--$SubNetID-->SubNetID<!--/$SubNetID--> has SQL Endpoints <Enabled> but there is no VNet firewall rules on target server <!--$ServerName-->ServerName<!--/$ServerName-->, causing the failure for given duration.

We identified that connections from client(s) in one or more Subnets are failing to connect to the database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->. This is caused by the VNet firewall rules for the {Server Name} not being configured for the Subnet(s) where the client is connecting from.  To properly allow connections from a VNet you will need to enable a firewall rule for the VNet/SubNet from which the client(s) are connecting. This is in addition to the SQL Endpoints that were enabled already for the respective subnet(s).
<!--/issueDescription-->

## **Recommended Documents**
https://docs.microsoft.com/en-us/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview
