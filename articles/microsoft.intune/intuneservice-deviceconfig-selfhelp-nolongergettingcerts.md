<properties
	pageTitle="User devices are no longer receiving SCEP certificates from NDES."
	description="User devices are no longer receiving SCEP certificates from NDES."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="13"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="deviceconfiguration_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="09ec1923-48fb-4b58-ae6e-274ffba61fa5"
	ownershipId="IntuneCxP_Intune"
/>

# User devices are no longer receiving SCEP certificates from NDES.

## **Recommended steps**

It is possible that the Client Authentication certificate issued to the NDES server and specified during the NDES connector installation has expired or is missing. To resolve this:

1. Uninstall the NDES connector. 
2. Use the following details to request a new client authentication or server authentication certificate:  
   * Subject name: CN=external fqdn 
   * Subject alternative name (both are required): 
      o	DNS=external fqdn
      o	DNS=internal fqdn 
3. Reinstall the NDES connector with the new certificate. 
4. Sign in to the NDES connector. 
5. Restart the NDES server. Wait 15 to 20 minutes and then sync a device.
