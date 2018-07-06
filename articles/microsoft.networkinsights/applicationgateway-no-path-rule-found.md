<properties
	pageTitle="Application Gateway - No Path Rule Found. Getting Defaults"
	description="Application Gateway - Rule is path-based but no path rules matched in URL path map."
	infoBubbleText="Rule is path-based but no path rules matched in the URL path map. See details on the right."
	service="microsoft.network"
	resource="Application Gateway"
	authors="cgeisbush"
	displayOrder="1"
	articleId="AppGwNoPathRuleFoundInsight"
	diagnosticScenario="AppGwChecklistInsights"
	selfHelpType="diagnostics"
	supportTopicIds="32436961,32573483,32582834"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public"
/>
#PLACEHOLDER ONLY - REPLACE ALL CONTENT BELOW
# We have detected degraded back-end server health for your Application Gateway

<!--issueDescription-->
Your Azure services appear to be running normally, however we have detected degraded health in the back-end server pool behind your Application Gateway **<!--$GatewayName-->Application Gateway<!--/$GatewayName-->** at **<!--$CurrentTime-->CurrentTime<!--/$CurrentTime--> (UTC)** 

- **Impacted Server:** <!--$BackendSeverAddress-->BackendSeverAddress<!--/$BackendSeverAddress--> 
- **Health Status:** <!--$HealthStatus-->HealthStatus<!--/$HealthStatus-->
- **Error Message:** <!--$ErrorDetails-->ErrorDetails<!--/$ErrorDetails-->  

The Application Gateway cannot reliably load balance requests when the back-end servers experience health issues.  When this occurs, you may not be able to reach the applications serviced by this gateway.
<!--/issueDescription-->

In order to FOO, you'll need to BAR.  You can use the following steps to help BLAH. 



1. Ensure your back-end server is up and running properly. (Exact steps will depend on the OS and service)
2. Check to ensure that the service can respond with HTTP 200 via alternate paths
3. If the service cannot respond with HTTP 200 to the Application Gateway probe, troubleshoot network connectivity including:  
    - Network Security Groups
    - Route tables
    - Network performance
    - General TCP connectivity troubleshooting

For additional help, you can refer to the article [Troubleshooting bad gateway errors in Application Gateway](http://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
