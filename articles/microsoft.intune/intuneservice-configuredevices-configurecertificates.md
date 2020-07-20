<properties
	pageTitle="Configure Devices - Configure certificates"
	description="Configure Devices - Configure certificates"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599605"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2682978a-12df-4f91-b72f-5afc7ebfac02"
	ownershipId="IntuneCxP_Intune"
/>

# Configure Devices - Configure certificates

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**When I try to install the Intune certificate connector on the NDES connector server, I get the message, "The password in the certificate request cannot be verified. It may have been used already. Obtain a new password to submit with this request."**

This message means that you need to run the certificate connector installation as an Administrator. For more information review the [documentation](https://docs.microsoft.com/intune/certificates-scep-configure). 

**User devices are no longer receiving SCEP certificates from NDES.**

It is possible that the Client Authentication certificate issued to the NDES server and specified during the NDES connector installation has expired or is missing. To resolve this:

1. Uninstall the NDES connector. 
2. Use the following details to request a new client authentication or server authentication certificate:  
   * Subject name: CN=external FQDN
   * Subject alternative name (both are required): DNS=external FQDN and DNS=internal FQDN
3. Reinstall the NDES connector with the new certificate. 
4. Sign in to the NDES connector. 
5. Restart the NDES server. Wait 15 to 20 minutes and then sync a device.

## **Recommended documents**

* [How to configure certificates in Microsoft Intune](https://docs.microsoft.com/intune/certificates-configure)<br>
* [Troubleshooting device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-troubleshoot)<br>
* [Configure and manage SCEP certificates with Intune](https://docs.microsoft.com/intune/certificates-scep-configure)<br>
* [Configure and manage PKCS certificates with Intune](https://docs.microsoft.com/intune/certficates-pfx-configure)<br>
* [Set up Intune Certificate Connector for Symantec PKI Manager Web Service](https://docs.microsoft.com/intune/certificates-symantec-configure)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
