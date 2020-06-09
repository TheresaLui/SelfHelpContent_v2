<properties
	pageTitle="I'm deploying a Wi-Fi profile that is dependent on a deployed certificate specified in the Wi-Fi profile. However, the configuration profiles are showing an error status"
	description="I'm deploying a Wi-Fi profile that is dependent on a deployed certificate specified in the Wi-Fi profile. However, the configuration profiles are showing an error status"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="deviceconfiguration_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7667ee89-6281-49eb-a677-f2b6cd156940"
	ownershipId="IntuneCxP_Intune"
/>

# I'm deploying a Wi-Fi profile that is dependent on a deployed certificate specified in the Wi-Fi profile. However, the configuration profiles are showing an error status.

## **Recommended steps**

Check that your device received the certificate.

1.	In Intune, go to **All Devices** and select the device > **Device configuration**. 
2.	Check that all expected profiles are listed and in a successful state.

If you have intermediate certificates in your certificate chain, make sure those are deployed to Android devices. To check the certificate status, go to **Device configuration > Profiles > Android intermediate CA > Properties > Trusted Certificate**.

If you continue to see errors, review the procedures and troubleshooting sections in the Intune [SCEP](https://docs.microsoft.com/intune/certificates-scep-configure) or [PKCS](https://docs.microsoft.com/intune/certficates-pfx-configure) documentation.
