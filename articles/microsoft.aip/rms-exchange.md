<properties
	pageTitle="RMS Connector - Exchange"
	description="RMS Connector - Exchange"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak,Uwe.Wizovsky"
	articleId="RMS_Connector_Exchange"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584345"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
/>

# RMS Connector - Exchange

## Recommended troubleshooting steps

Please be sure you meet the pre-requisites here:
[Configuring an Exchange server to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-an-exchange-server-to-use-the-connector)
Please also check the registry settings are defined correctly depending on your Exchange Server version as outlined here:
[Exchange 2013 and 2016](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#exchange-2016-or-exchange-2013-registry-settings)
[Exchange 2010](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#exchange-2010-registry-settings)

## Potential issues:
Users cannot use Exchange IRM features, like OWA
1.	Is user able to open email in Outlook? If no, not a connector issue, drive to Office or Microsoft RMS queues.

2.	Is this specific to one user or a specific piece of content? If yes, go to #7

3.	In Exchange, use Test-IRMConfiguration. If it works, go to #6

4.	Check Exchange configuration with:
	a.	Get-IRM configuration. Check that it is:
	InternalLicensingEnabled       : True
	ExternalLicensingEnabled       : False
	JournalReportDecryptionEnabled : True/False
	ClientAccessServerEnabled      : True
	SearchEnabled                  : True/False
	TransportDecryptionSetting     : Any
	EDiscoverySuperUserEnabled     : True
	ServiceLocation                : MicrosoftRMSUrl
	PublishingLocation             : MicrosoftRMSUrl
	LicensingLocation              : MicrosoftRMSUrl
	If either value is wrong, correct it via Set-IRMConfiguration
	b.	If the Locations are wrong, fix the following locations in the Registry:
	HKLM\Software\Microsoft\MSDRM\ServiceLocation\Activation Reg_SZ: Default = "https://MicrosoftRMSURL/_wmcs/certification"
	and purge certificates in the Exchange DRM folder in each Exchange server, disable and re-enable IRM. Keep in mind that different Exchange servers may have different registry settings, all should have the same.

5.	Check Connector logs. An event 1002 should indicate if Exchange is actually trying to connect to the connector. If not present on any connector node, most likely Exchange is either running the wrong software version (must be 2010 CU2 or 2013 RU1) or not configured with the redirection URLs in registry as follows:
HKLM\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\CertificationServerRedirection Reg_SZ:"https://MicrosoftRMSURL/_wmcs/certification" = "http(s)://connectorName/_wmcs/certification"  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\LicenseServerRedirection Reg_SZ: "https://MicrosoftRMSURL/_wmcs/licensing" = "http(s)://connectorName/_wmcs/licensing"
It may also indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above (connectorname/_wmcs/licensing). If you see an IIS error, it is OK. If you don’t get a response, most likely DNS, IP or load balancing error is occurring. Also check if SSL is correctly specified in the registry and if it is being used if it is working. 
An event 2001 indicates that the server is not authorized to use the connector. The identity utilized by Exchange to utilize the connector is not listed in the Connector Authorizations list. Open the Connector administration tool and check if the Exchange Servers group, or any group containing all the Exchange Servers server accounts, is listed in the authorizations.
An event 3000 indicates that the Connector is not properly configured to talk to Microsoft RMS or that its authorization certificates are invalid. Connector node needs to be reinstalled.

6.	If a specific server can’t consume the content but others can’t, check if the server may be authorized via a different rule than the other servers (either it was authorized individually or it belongs to another group also authorized to use the connector) or if the rule is not specified as an Exchange server. Also check registry keys as above. 

7.	Check if user and group membership is properly replicated in AAD. 
Check if user has rights to the content in Outlook. 
Check if resending the content after unprotecting and re-protecting works (may have been prelicensed before the user got the right group membership or group membership was cached). 

8.	Additional possible causes:
	a.	SSL CRL not accessible
	b.	SSL certificate in connector not trusted by Exchange servers
	c.	Wrong MSDRM version in Exchange server (needs to be Mode 2 capable client as per http://technet.microsoft.com/en-us/library/hh867439(v=ws.10).aspx#BKMK_Pre ). 

<br>
	
## The Admin cannot enable the IRM Integration in Exchange
1.	In Exchange, use Test-IRMConfiguration. If it works, go to #6

2.	Check Exchange configuration with:
	a.	Get-IRM configuration. Check that it is:
	InternalLicensingEnabled       : True
	ExternalLicensingEnabled       : False
	JournalReportDecryptionEnabled : True/False
		ClientAccessServerEnabled      : True
	SearchEnabled                  : True/False
	TransportDecryptionSetting     : Any
	EDiscoverySuperUserEnabled     : True
	ServiceLocation                : MicrosoftRMSUrl
	PublishingLocation             : MicrosoftRMSUrl
	LicensingLocation              : MicrosoftRMSUrl
	If either value is wrong, correct it via Set-IRMConfiguration
	b.	If the Locations are wrong, fix the following locations in the Registry:
	HKLM\Software\Microsoft\MSDRM\ServiceLocation\Activation Reg_SZ: Default = "https://MicrosoftRMSURL/_wmcs/certification"
	and purge certificates in the Exchange DRM folder in each Exchange server, disable and re-enable IRM. Keep in mind that different Exchange servers may have different registry settings, all should have the same.

3.	Check Connector logs. An event 1002 should indicate if Exchange is actually trying to connect to the connector. If not present on any connector node, most likely Exchange is either running the wrong software version (must be 2010 CU2 or 2013 RU1) or not configured with the redirection URLs in registry as follows:
HKLM\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\CertificationServerRedirection Reg_SZ:"https://MicrosoftRMSURL/_wmcs/certification" = "http(s)://connectorName/_wmcs/certification"  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\LicenseServerRedirection Reg_SZ: "https://MicrosoftRMSURL/_wmcs/licensing" = "http(s)://connectorName/_wmcs/licensing"
It may also indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above (http(s)://connectorname/_wmcs/licensing). If you see an IIS error, it is OK. If you don’t get a response, most likely DNS, IP or load balancing error is occurring. Also check if SSL is correctly specified in the registry and if it is being used if it is working. 
An event 2001 indicates that the server is not authorized to use the connector. The identity utilized by Exchange to utilize the connector is not listed in the Connector Authorizations list. Open the Connector administration tool and check if the Exchange Servers group, or any group containing all the Exchange Servers server accounts, is listed in the authorizations.
An event 3000 indicates a general error in the Connector. This may be caused by the Connector not being properly configured to talk to Microsoft RMS or that its authorization certificates are invalid. Reinstall the Connector node and see if this solves the problem.

4.	If a specific server can’t consume the content but others can’t, check if the server may be authorized via a different rule than the other servers (either it was authorized individually or it belongs to another group also authorized to use the connector) or if the rile is not specified as an Exchange server. Also check registry keys as above. 

5.	Check if user and group membership for the test account is properly replicated in AAD. 
Check if user has rights to the content in Outlook. 
Check if resending the content after unprotecting and re-protecting works (may have been prelicensed before the user got the right group membership or group membership was cached). 

6.	Additional possible problems:
	a.	SSL CRL not accessible
	b.	SSL certificate in connector not trusted by Exchange servers
	c.	Wrong MSDRM version in Exchange server (needs to be Mode 2 capable client as per http://technet.microsoft.com/en-us/library/hh867439(v=ws.10).aspx#BKMK_Pre). 

	If that fails does not help

Create an RMS Analyzer trace on the Exchange Server and a RMS connector Trace at the same time.
RMS connector as described here: [Logging](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector#logging)<br>

RMS Analyzer:
Download from here: [Download RMS Analyzer](https://www.microsoft.com/download/details.aspx?id=46437)
Start as local admin.
Go straight to the logging tab
Start logging
Reproduce the issue
Afterwards stop logging
Attach the create zip/cab file to the support call and explain what you are trying to do

## **Recommended Documents**

[Deploying the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/deploy-rms-connector )<br>
[Installing and configuring the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/install-configure-rms-connector)<br>
[Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
[Configuring servers for the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector)<br>
[Registry setting for the Rights Management connector](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings)