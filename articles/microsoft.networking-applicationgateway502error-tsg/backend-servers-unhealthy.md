<properties
	  pageTitle="TSG Content Step: Check if the backend servers are unhealthy"
	  description="TSG Content Step: Check if the backend servers are unhealthy"
	  service="microsoft.network"
	  resource="applicationGateway"
	  authors="JRMayberry"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="49792fac-d334-4c08-8a4f-f2d582bac362"
	ownershipId="CloudNet_AzureApplicationGateway"
/>


 # How to check if all the backend servers are unhealthy which could cause Application Gateway to return HTTP 502 to the client:

1. Identify the HTTP Settings and Backend Pool that is tied to the listener by the Rule from the **Request Routing Rules** in ASC.
2. Go to **Diagnostics** tab of ASC Resource Explorer of the AppGW and scroll down to find the link for *Backend Service Diagnostics History MDM Log*. 
Alternatively, you can check the table from [Jarvis Logs -> AppGWT -> BackendServerDiagnosticHistory](https://jarvis-west.dc.ad.msft.net/BEA88EA9).
3. Check the Healthy column for the respective backend pool and HTTP setting combination if the value for all the servers are True or False. If it is True, then the server was healthy for that port and probe combination at the time of logging. If it is False, then the server was unhealthy.
4. Alternatively, you can ask the customer to check the **Backend Health** blade in the Application Gateway menu from the Azure Portal to get the result.
