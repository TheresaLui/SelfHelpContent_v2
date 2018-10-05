properties
	pageTitle="Database Connectivity issue due VNet Rules"
	description="VNetRuleIssue"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	displayOrder=""
	articleId="vNetIssue_96EAE137-BB69-4B9E-863A-72D23CBFE32F "
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="32589555"
	resourceTags=""
	productPesIds="13491" 
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->

Connections for database originating from  Subnet : *<!--$SubNetID--> SubNetID <!--/$SubNetID-->**}  has SQL Endpoints <Enabled> but there is no VNet firewall rules on the target, causing the failure for the given duration.<br>
 
 ENVIRONMENT: <br>
 ServerName : {ServerName} <br>
 DatabaseName : {DatabaseName} <br> 
 Impact timeframe: Between {StartTime} and {EndTime} <br>
 
<!--/issueDescription-->

**Root cause investigation**<br>
We identified that connections from client(s) in one or more Subnets are failing to connect to the database {Database Name} on {Server Name}.  This is caused by the VNet firewall rules for the {Server Name} not being configured for the Subnet(s) where the client is connecting from.  To properly allow connections from a VNet you will need to enable a firewall rule for the VNet from which the client(s) are connecting.  This is in addition to the SQL Endpoints that were enabled already for the respective subnet(s). <br>
	
The documentation on how to configure this as well as other information on this topic can be found at the below article. <br><br>

Azure is continuing to refine the above signals as more telemetry is analyzed.<br>
