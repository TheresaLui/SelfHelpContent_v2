<properties
	pageTitle="Degraded Backend Server Health"
	description="Application Gateway - Backend server health degraded"
	infoBubbleText="Backend server health degraded for the application gateway. See details on the right."
	service="microsoft.network"
	resource="Application Gateway"
	authors="cgeisbush"
	ms.author="chgeis"
	displayOrder="1"
	articleId="AppGwDegradedBackendServerHealthInsight"
	diagnosticScenario="AppGwChecklistInsights"
	selfHelpType="diagnostics"
	supportTopicIds="32436961,32573483,32582834"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# We have detected degraded back-end server health for your Application Gateway

<!--issueDescription-->
Your Azure services appear to be running normally, however we have detected degraded health in the back-end server pool behind your Application Gateway **<!--$GatewayName-->Application Gateway<!--/$GatewayName-->** at **<!--$CurrentTime-->CurrentTime<!--/$CurrentTime--> (UTC)**
<!--/issueDescription-->

- **Impacted Server:** <!--$BackendSeverAddress-->BackendSeverAddress<!--/$BackendSeverAddress-->
- **Health Status:** <!--$HealthStatus-->HealthStatus<!--/$HealthStatus-->
- **Error Message:** <!--$ErrorDetails-->ErrorDetails<!--/$ErrorDetails--> 

The Application Gateway cannot reliably load balance requests when the back-end servers experience health issues.  When this occurs, you may not be able to reach the applications serviced by this gateway.

In order to restore functionality, you'll need to first determine the cause of the issue at the back-end server.  You can use the following steps to help troubleshoot the issue.

## **Recommended Steps**

1. Ensure your back-end server is up and running properly (exact steps will depend on the OS and service)
2. Check to ensure that the service can respond with HTTP 200 via alternate paths
3. If the service cannot respond with HTTP 200 to the Application Gateway probe, troubleshoot network connectivity including:  

    - Network Security Groups
    - Route tables
    - Network performance
    - General TCP connectivity troubleshooting

## **Recommended Documents**

* [Troubleshooting bad gateway errors in Application Gateway](http://docs.microsoft.com/azure/application-gateway/application-gateway-troubleshooting-502)
