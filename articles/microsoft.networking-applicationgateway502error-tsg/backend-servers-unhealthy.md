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

# Check backend server health

## How to check if all the backend servers are unhealthy which could cause Application Gateway to return HTTP 502 to the client

HTTP error 502 indicates that the Application Gateway is not able to connect to the backend, implying either the backend is down or there is a reachability issue. It does not matter the kind of backend - it can be an APIM, Docker, VMSS or VM in the backend, but the service should be up and reachable. Below are some steps that can isolate and help resolve the issue.

1. The backend must be up. It's worth to note that the issue can also be on the backend because of which Application Gateway is not able to connect. Ensure we have the backend healthy and connections are allowed. Service should be up and SSL certificates should be configured correctly.
1. The backend must be reachable. Check the NSGs or firewall rules on the source Application Gateway and the destination backend.
1. Identify the HTTP Settings and Backend Pool that is tied to the listener by the Rule from the **Request Routing Rules** in ASC.
1. Go to **Diagnostics** tab of ASC Resource Explorer of the AppGW and scroll down to find the link for *Backend Service Diagnostics History MDM Log Link*. 
Alternatively, you can check the table from Jarvis Logs -> AppGWT -> [BackendServerDiagnosticHistory](https://jarvis-west.dc.ad.msft.net/logs/dgrep?page=logs&be=DGrep&offset=-30&offsetUnit=Minutes&UTC=true&ep=Diagnostics%20PROD&ns=AppGWT&en=BackendServerDiagnosticHistory&scopingConditions=[["__Region__",""],["GatewayId",""]]&conditions=[]&clientQuery=orderby%20TIMESTAMP%20asc&aggregates=["Count%20by%20RoleInstance","Count%20by%20backend_routed","Count%20by%20httpMethod","Count%20by%20backend_httpStatus","Count%20by%20appgw_httpStatus"]&chartEditorVisible=true&chartType=Line&chartLayers=[["New%20Layer",""]]%20)
1. You must also refer to [InformationLogEvent](https://jarvis-west.dc.ad.msft.net/logs/dgrep?page=logs&be=DGrep&offset=-30&offsetUnit=Minutes&UTC=true&ep=Diagnostics%20PROD&ns=AppGWT&en=InformationLogEvent&scopingConditions=[["__Region__",""],["GatewayId",""]]&conditions=[]&clientQuery=orderby%20TIMESTAMP%20asc&aggregates=["Count%20by%20RoleInstance","Count%20by%20backend_routed","Count%20by%20httpMethod","Count%20by%20backend_httpStatus","Count%20by%20appgw_httpStatus"]&chartEditorVisible=true&chartType=Line&chartLayers=[["New%20Layer",""]]%20) table, this is helpful at times, e.g. if the problem is due to an SSL-related error.
1. Check the Healthy column for the respective backend pool and HTTP setting combination if the value for all the servers are True or False. If it is True, then the server was healthy for that port and probe combination at the time of logging. If it is False, then the server was unhealthy.
1. Alternatively, you can ask the customer to check the **Backend Health** blade in the Application Gateway menu from the Azure Portal to get the result.
