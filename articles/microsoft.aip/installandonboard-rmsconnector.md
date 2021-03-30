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

1. Ensure that you meet the prerequisites to [configure an Exchange server to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-an-exchange-server-to-use-the-connector).<br>
2. Check that the registry settings are defined correctly for your specific Exchange Server version:

	* [Exchange 2013 and 2016](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#exchange-2016-or-exchange-2013-registry-settings)
	* [Exchange 2010](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#exchange-2010-registry-settings)

3. Review the steps to [configure a SharePoint server to use the connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector#configuring-a-sharepoint-server-to-use-the-connector)<br>
4. Review and update (if necessary) your [SharePoint 2016 or SharePoint 2013 registry settings](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings#sharepoint-2016-or-sharepoint-2013-registry-settings)<br>

### Potential Issues

### Admin cannot enable IRM in SharePoint

1. Check the SharePoint Admin UI to ensure the server is configured with the **Use this RMS server** option, and it is pointed manually to the *Connector* URL, and not to the *Microsoft RMS* URL)
2. If you are using SharePoint 2013, check the MSIPC version in the SharePoint server. The MSIPC version must be 2.1 or later.
3. Check the event logs for each connector server. 

    - If there are no **1002** events, it may indicate a problem with the DNS pointer or with load balancing. In this case, try to access the RMS URLs from a web browser in an Exchange server, as specified in the registry entries as above - https://connectorURL/_wmcs/licensing. 

        If you see an IIS error, it is OK. If you don’t get a response, most likely a DNS, IP, or load balancing error is occurring. 

        Also check if SSL is correctly specified in the registry, and if it's being used if it's working.

    - **Event 2001** indicates that the server is not authorized to use the connector, and that the identity used by SharePoint to use the connector is not listed in the Connector Authorizations list. 
    
        Open the Connector administration tool and verify whether the service account used by the SharePoint Global Administration service is explicitly authorized, or if one, and only one, group containing this account is authorized.

        If SharePoint is NOT configured to use a service account, which is the best practice, then the computer account **(SERVERNAME$)** or a group containing it must be authorized instead.<br>

    - **Event 3000** indicates that the Connector is not properly configured to talk to Microsoft RMS, or that its authorization certificates are invalid. In this case, the connector node must be reinstalled.

Additional possible causes:

* SSL CRL not accessible
* SSL certificate in connector not trusted by Exchange servers
* Incorrect MSDRM version in the Exchange server. The MSDRM version must be a [Mode 2 capable client](https://aka.ms/rms-exchange).
	
**Users cannot use Exchange IRM features, like OWA**

1. Is user able to open email in Outlook? If not, you don't have a connector issue. Navigate to the Office or Microsoft RMS support queues and create a ticket.
2. Is your issue specific to one user, or a specific piece of content? If yes, skip to step #7 below.
3. In Exchange, use the [Test-IRMConfiguration](https://docs.microsoft.com/powershell/module/exchange/Test-IRMConfiguration) cmdlet. If it works, skip to step #6 below.
4. Check the Exchange configuration as follows:<br>

    - Use the [Get-IRMConfiguration](https://docs.microsoft.com/powershell/module/exchange/Get-IRMConfiguration) cmdlet. Check that it has the following values:<br>

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

        If any of the values listed above are incorrect, correct them using the [Set-IRMConfiguration](https://docs.microsoft.com/powershell/module/exchange/set-irmconfiguration) cmdlet.
	
        If the location values are incorrect, fix the following locations in the Registry:<br>
	
        ```
        HKLM\Software\Microsoft\MSDRM\ServiceLocation\Activation Reg_SZ: Default = "https://MicrosoftRMSURL/_wmcs/certification"
        ```

    - Purge certificates in the Exchange DRM folder in each Exchange server, and then disable and re-enable IRM. Keep in mind that different Exchange servers may have different registry settings. All servers should have the same settings.<br>

5. Check Connector logs. 

    - **Event 1002** should indicate if Exchange is actually trying to connect to the connector. 

        If this event not present on any connector node, it is most likely that Exchange is either running an incorrect software version (must be 2010 CU2 or 2013 RU1), or not is configured with the redirection URLs in the registry, as follows:<br>

        ```
        HKLM\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\CertificationServerRedirection Reg_SZ:"https://MicrosoftRMSURL/_wmcs/certification" = "http(s)://connectorName/_wmcs/certification"

        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\LicenseServerRedirection Reg_SZ: "https://MicrosoftRMSURL/_wmcs/licensing" = "http(s)://connectorName/_wmcs/licensing"
        ```

        It may also indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server as specified in the registry entries as above (`connectorname/_wmcs/licensing`). 

        If you see an IIS error, it is OK. If you don’t get a response, most likely a DNS, IP, or load balancing error is occurring. Also check whether SSL is correctly specified in the registry, and if it is being used if it is working.

    - **Event 2001** indicates that the server is not authorized to use the connector, and the identity used by Exchange to used the connector is not listed in the Connector Authorizations list. 
    
        Open the Connector administration tool and check if the Exchange Servers group, or any group containing all the Exchange Servers server accounts, is listed in the authorizations.

    - **Event 3000** indicates that the Connector is not properly configured to talk to Microsoft RMS, or that its authorization certificates are invalid. In this case, the connector node must be reinstalled.

6. If a specific server can't consume the content but others can, check if one of the following applies:

    - If the server is authorized via a different rule than the other servers, either authorized individually or by belonging to another group also authorized to use the connector
    - If the rule is not specified as an Exchange server. 
    
    Additionally, check the registry keys as described above.

1. Check the following:

    - Whether the user and group membership is properly replicated in Azure Active Directory. 
    - Whether the user has rights to the content in Outlook.
    - Whether resending the content after unprotecting and re-protecting works. If this works, it may have been pre-licensed before the user obtained the correct group membership, or if the group membership was cached.

Additional possible causes:

* SSL CRL is not accessible
* SSL certificate in the connector is not trusted by the Exchange servers
* Incorrect MSDRM version in the Exchange server. The MSDRM version must be a [Mode 2 capable client](https://aka.ms/rms-exchange).
	
### The Admin cannot enable the IRM Integration in Exchange

1. In Exchange, use Test-IRMConfiguration. If it works, go to #6
2. Check Exchange configuration with:<br>

    * Get-IRMConfiguration cmdlet. Check that it is:<br>
	
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

        If any of the values are incorrect, correct them using the Set-IRMConfiguration cmdlet.<br>
    
        If the locations are defined incorrectly, fix the following locations in the Registry:
	
        ```
        HKLM\Software\Microsoft\MSDRM\ServiceLocation\Activation Reg_SZ: Default = "https://MicrosoftRMSURL/_wmcs/certification"
        ```

    * Purge certificates in the Exchange DRM folder in each Exchange server, and then disable and re-enable IRM. 

        Keep in mind that different Exchange servers may have different registry settings - all servers should have the same settings.<br>

3. Check the Connector logs for the following events: 

    - **Event 1002** should indicate if Exchange is actually trying to connect to the connector. If it not present on any connector node, most likely Exchange is either running an incorrect software version (must be 2010 CU2 or 2013 RU1) or is not configured with the redirection URLs in the registry, as follows:<br>

        ```
        HKLM\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\CertificationServerRedirection Reg_SZ:"https://MicrosoftRMSURL/_wmcs/certification" = "https://connectorName/_wmcs/certification"

        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ExchangeServer\(v14|v15)\IRM\LicenseServerRedirection Reg_SZ: "https://MicrosoftRMSURL/_wmcs/licensing" = "https://connectorName/_wmcs/licensing"
        ```

        It may also indicate a problem with the DNS pointer or with load balancing. Try to access the RMS URLs from a web browser in an Exchange server, as specified in the registry entries listed above - https://connectorname/_wmcs/licensing. 

        If you see an IIS error, it is OK. If you don’t get a response, most likely a DNS, IP or load balancing error is occurring. 

        Also check whether SSL is correctly specified in the registry, and if it is being used if it is working.

    - **Event 2001** indicates that the server is not authorized to use the connector, and that the identity used by Exchange to use the connector is not listed in the Connector Authorizations list. 
    
        Open the Connector administration tool and check whether the Exchange Servers group, or any group containing all the Exchange Servers server accounts, is listed in the authorizations.

    - **Event 3000** indicates a general error in the Connector. This may be caused by the Connector not being properly configured to talk to Microsoft RMS, or that its authorization certificates are invalid. 
    
        Reinstall the Connector node and see if this solves the problem.

4. If a specific server can’t consume the content, but others can, check:

    - Whether the server might be authorized via a different rule than the other servers (either it was authorized individually or it belongs to another group also authorized to use the connector)
    - Whether the rile is not specified as an Exchange server.
    - Check registry keys, as described above.
1. Check the following regarding user and group configuration:
    - If user and group membership for the test account is properly replicated in Azure Active Directory. 
    - If the user has rights to the content in Outlook. 
    - If resending the content after un-protecting and re-protecting works (may have been pre-licensed before the user obtained the right group membership, or the group membership was cached).
1. Additional possible issues:
	* The SSL CRL is not accessible
	* The SSL certificate in the connector is not trusted by the Exchange servers
	* An incorrect MSDRM version in Exchange server - the MSDRM version must be a [Mode 2 capable client](https://aka.ms/rms-exchange).

## **Recommended Documents**

* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Deploying the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/deploy-rms-connector )<br>
* [Installing and configuring the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/install-configure-rms-connector)<br>
* [Monitor the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/monitor-rms-connector)<br>
* [Configuring servers for the Azure Rights Management connector](https://docs.microsoft.com/azure/information-protection/configure-servers-rms-connector)<br>
* [Registry setting for the Rights Management connector](https://docs.microsoft.com/azure/information-protection/rms-connector-registry-settings)
