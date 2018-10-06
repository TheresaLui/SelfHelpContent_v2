<properties
	pageTitle="Database connectivity - Proxy Throttling issue"
	description="Proxythrottle"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="hsuyiting"
	displayOrder=""
	articleId="IsProxyThrottling_0A86E0B4-1C26-4ACD-9B95-C6296829B8D8"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds="31980402"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that connections utilizing the Proxy method of connecting to the  {DatabaseName} on {ServerName} were being throttled.  By default, connections originating outside of the Azure network boundary will use the proxy method which will be a shared common endpoint for connecting to the database(s) in that region.  If performance regressions are seen or heavy traffic from a client are seen, throttling can occur. 


When using the proxy method, only the 1433 outbound port from the clients network needs to be allowed. Clients within Azure are identified and use the redirect method which during the connection process will be provided a redirect token indicating the specific endpoint of the SQL database.  This instance will be listening on a dynamic port within the range of 11000-11999 and 14000-14999 which will require the network where the client resides to allow those outbound ports in addition to the standard 1433 port for SQL.
 

If this is causing issues for your application workload you can force all connections to your database to use the redirect method to connect, avoiding the potential of this scenario occurring. The below document discusses the connectivity architecture for Azure SQL DB but also includes steps to force redirect method for all connections.

 
<!--/issueDescription-->

