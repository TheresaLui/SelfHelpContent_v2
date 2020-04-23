<properties
	pageTitle="Azure Information Protection - Installing, Onboarding, or Decommissioning - RMS connector setup and configuration"
	description="Azure Information Protection - Installing, Onboarding, or Decommissioning - RMS connector setup and configuration"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727966"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="MIP_Onboard_Install_rmsconnector"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection  - Installing, Onboarding, or Decommissioning - My scenario is not listed

## **Recommended Steps for RMS Connector with Exchange/SharePoint**

1. Ensure you meet the prerequisites to [configure an Exchange server to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-an-exchange-server-to-use-the-connector)<br>
2. Check the registry settings are defined correctly for your specific Exchange Server version:

	* [Exchange 2013 and 2016](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#exchange-2016-or-exchange-2013-registry-settings)
	* [Exchange 2010](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#exchange-2010-registry-settings)

3. Review the steps to [configure a SharePoint server to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-a-sharepoint-server-to-use-the-connector)<br>
4. Review and update (if necessary) your [SharePoint 2016 or SharePoint 2013 registry settings](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#sharepoint-2016-or-sharepoint-2013-registry-settings)<br>

### Potential Issues

### Admin cannot enable IRM in SharePoint

1. Check the SharePoint Admin UI to ensure the server is configured with the "Use this RMS server" and it is pointed manually to the Connector URL (not to the Microsoft RMS URL)
2. If using SharePoint 2013, check the MSIPC version in the SharePoint server - it must be 2.1 or later
3. Check event logs in each connector server. If there are no 1002 events it may indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above - https://connectorURL/_wmcs/licensing. If you see an IIS error, it is OK. If you don’t get a response, most likely a DNS, IP, or load balancing error is occurring. Also check if SSL is correctly specified in the registry and if it is being used if it is working.
4. **Event 2001** indicates that the server is not authorized to use the connector. The identity utilized by SharePoint to utilize the connector is not listed in the Connector Authorizations list. Open the Connector administration tool and check if the service account utilized by the SharePoint Global Administration service is explicitly authorized or if one, and only one, group containing this account is authorized. If SharePoint is NOT configured to use a service account (which is the best practice) then the computer account (SERVERNAME$) or a group containing it needs to be authorized.<br>
5. **Event 3000** indicates that the Connector is not properly configured to talk to Microsoft RMS or that its authorization certificates are invalid. Connector node needs to be reinstalled.
6. Additional possible causes:

	* SSL CRL not accessible
	* SSL certificate in connector not trusted by Exchange servers
	* Wrong MSDRM version in Exchange server - must be [Mode 2 capable client](https://aka.ms/rms-exchange)
	
**Users cannot use Exchange IRM features, like OWA**

1. Is user able to open email in Outlook? If no, it is not a connector issue. Navigate to Office or Microsoft RMS support queues and create a ticket.
2. Is this specific to one user or a specific piece of content? If yes, go to #7
3. In Exchange, use Test-IRMConfiguration. If it works, go to #6
4. Check Exchange configuration with:<br>

* Get-IRM configuration. Check that it is:<br>

```
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
```

If either value is wrong, correct it via Set-IRMConfiguration.
	
* If the Locations are wrong, fix the following locations in the Registry:<br>
	
```
HKLM\Software\Microsoft\MSDRM\ServiceLocation\Activation Reg_SZ: Default = "https://MicrosoftRMSURL/_wmcs/certification"
```

Purge certificates in the Exchange DRM folder in each Exchange server, then disable and re-enable IRM. Keep in mind that different Exchange servers may have different registry settings - all servers should have the same settings.<br>

5. Check Connector logs. **Event 1002** should indicate if Exchange is actually trying to connect to the connector. If not present on any connector node, it is most likely that Exchange is either running the wrong software version (must be 2010 CU2 or 2013 RU1), or not is configured with the redirection URLs in registry as follows:<br>

```
HKLM\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\CertificationServerRedirection Reg_SZ:"https://MicrosoftRMSURL/_wmcs/certification" = "http(s)://connectorName/_wmcs/certification"

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\LicenseServerRedirection Reg_SZ: "https://MicrosoftRMSURL/_wmcs/licensing" = "http(s)://connectorName/_wmcs/licensing"
```

It may also indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above (connectorname/_wmcs/licensing). If you see an IIS error, it is OK. If you don’t get a response, most likely DNS, IP, or load balancing error is occurring. Also check if SSL is correctly specified in the registry and if it is being used if it is working.

**Event 2001** indicates that the server is not authorized to use the connector. The identity utilized by Exchange to utilize the connector is not listed in the Connector Authorizations list. Open the Connector administration tool and check if the Exchange Servers group, or any group containing all the Exchange Servers server accounts, is listed in the authorizations.

**Event 3000** indicates that the Connector is not properly configured to talk to Microsoft RMS or that its authorization certificates are invalid. Connector node needs to be reinstalled.

6. If a specific server can't consume the content but others can, check if the server may be authorized via a different rule than the other servers (either it was authorized individually or it belongs to another group also authorized to use the connector) or if the rule is not specified as an Exchange server. Also check registry keys as above.
7. Check if user and group membership is properly replicated in AAD. Check if user has rights to the content in Outlook.
Check if resending the content after unprotecting and re-protecting works (may have been pre-licensed before the user got the right group membership or group membership was cached).

8. Additional possible causes:

	* SSL CRL not accessible
	* SSL certificate in connector not trusted by Exchange servers
	* Wrong MSDRM version in Exchange server - must be [Mode 2 capable client](https://aka.ms/rms-exchange)
	
### The Admin cannot enable the IRM Integration in Exchange

1. In Exchange, use Test-IRMConfiguration. If it works, go to #6
2. Check Exchange configuration with:<br>

* Get-IRM configuration. Check that it is:<br>
	
```
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
```

If either value is wrong, correct it via Set-IRMConfiguration<br>

* If the Locations are wrong, fix the following locations in the Registry:
	
```
HKLM\Software\Microsoft\MSDRM\ServiceLocation\Activation Reg_SZ: Default = "https://MicrosoftRMSURL/_wmcs/certification"
```

Purge certificates in the Exchange DRM folder in each Exchange server, then disable and re-enable IRM. Keep in mind that different Exchange servers may have different registry settings - all servers should have the same settings.<br>

3. Check Connector logs. **Event 1002** should indicate if Exchange is actually trying to connect to the connector. If not present on any connector node, most likely Exchange is either running the wrong software version (must be 2010 CU2 or 2013 RU1) or not configured with the redirection URLs in registry as follows:<br>

```
HKLM\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\CertificationServerRedirection Reg_SZ:"https://MicrosoftRMSURL/_wmcs/certification" = "https://connectorName/_wmcs/certification"

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\LicenseServerRedirection Reg_SZ: "https://MicrosoftRMSURL/_wmcs/licensing" = "https://connectorName/_wmcs/licensing"
```

It may also indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above - https://connectorname/_wmcs/licensing. If you see an IIS error, it is OK. If you don’t get a response, most likely DNS, IP or load balancing error is occurring. Also check if SSL is correctly specified in the registry and if it is being used if it is working.

**Event 2001** indicates that the server is not authorized to use the connector. The identity utilized by Exchange to utilize the connector is not listed in the Connector Authorizations list. Open the Connector administration tool and check if the Exchange Servers group, or any group containing all the Exchange Servers server accounts, is listed in the authorizations.

**Event 3000** indicates a general error in the Connector. This may be caused by the Connector not being properly configured to talk to Microsoft RMS or that its authorization certificates are invalid. Reinstall the Connector node and see if this solves the problem.

4. If a specific server can’t consume the content but others can’t, check if the server may be authorized via a different rule than the other servers (either it was authorized individually or it belongs to another group also authorized to use the connector) or if the rile is not specified as an Exchange server. Also check registry keys as above.
5. Check if user and group membership for the test account is properly replicated in AAD. Check if user has rights to the content in Outlook. Check if resending the content after unprotecting and re-protecting works (may have been pre-licensed before the user got the right group membership or group membership was cached).
6. Additional possible problems:

	* SSL CRL not accessible
	* SSL certificate in connector not trusted by Exchange servers
	* Wrong MSDRM version in Exchange server - must be [Mode 2 capable client](https://aka.ms/rms-exchange)

## **Recommended Documents**

* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Deploying the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/deploy-rms-connector )<br>
* [Installing and configuring the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/install-configure-rms-connector)<br>
* [Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
* [Configuring servers for the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector)<br>
* [Registry setting for the Rights Management connector](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings)
