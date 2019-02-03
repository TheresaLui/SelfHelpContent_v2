<properties
	pageTitle="RMS Connector - SharePoint"
	description="RMS Connector - SharePoint"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak,Uwe.Wizovsky"
	articleId="RMS_Connector_SharePoint"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584375"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# RMS Connector - SharePoint

## Recommended troubleshooting steps

Please read the following info: [Configuring a SharePoint server to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-a-sharepoint-server-to-use-the-connector)<br>
Please check the registry settings are defined as well as described here:[SharePoint 2016 or SharePoint 2013 registry settings](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#sharepoint-2016-or-sharepoint-2013-registry-settings)<br>


## Potential issues:

## Admin cannot enable IRM in SharePoint

1.	Check the SharePoint Admin UI, that the server is configured with the “Use this RMS server” and pointing it manually to the Connector URL (not to the Microsoft RMS URL). 

2.	If using SharePoint 2013 check the MSIPC version in the SharePoint server. Must be 2.1 or later. 

3.	Check event logs in each connector server. If there are no 1002 events it may indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above - https://connectorURL/_wmcs/licensing. If you see an IIS error, it is OK. If you don’t get a response, most likely DNS, IP or load balancing error is occurring. Also check if SSL is correctly specified in the registry and if it is being used if it is working. <br>
	An event 2001 indicates that the server is not authorized to use the connector. The identity utilized by SharePoint to utilize the connector is not listed in the Connector Authorizations list. Open the Connector administration tool and check if the service account utilized by the SharePoint Global Administration service is explicitly authorized or if one, and only one, group containing this account is authorized. If SharePoint is NOT configured to use a service account (which is the best practice) then the computer account (SERVERNAME$) or a group containing it needs to be authorized.<br>
	An event 3000 indicates that the Connector is not properly configured to talk to Microsoft RMS or that its authorization certificates are invalid. Connector node needs to be reinstalled.

4.	Additional possible causes:
	a.	SSL CRL not accessible
	b.	SSL certificate in connector not trusted by Exchange servers
	c.	Wrong MSDRM version in Exchange server (needs to be Mode 2 capable client as per http://technet.microsoft.com/library/hh867439(v=ws.10).aspx#BKMK_Pre). 

	

	If all of the above didn't help, please collect the below logs and add them to your suppot ticket

Create an RMS Analyzer trace on the Exchange Server and a RMS connector Trace at the same time.<br>

RMS connector as described here: [Logging](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector#logging)<br>

RMS Analyzer:<br>
Download from here: [Download RMS Analyzer](https://www.microsoft.com/download/details.aspx?id=46437)<br>
Start as local admin.<br>
Go straight to the logging tab<br>
Start logging<br>
Reproduce the issue<br>
Afterwards stop logging<br>
Attach the create zip/cab file to the support call and explain what you are trying to do<br>



## **Recommended Documents**

[Deploying the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/deploy-rms-connector )<br>
[Installing and configuring the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/install-configure-rms-connector)<br>
[Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
[Configuring servers for the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector)<br>
[Registry setting for the Rights Management connector](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings)