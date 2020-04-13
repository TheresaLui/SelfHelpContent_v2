<properties
	pageTitle="Configure Devices - Configure Wifi Settings"
	description="Configure Devices - Configure Wifi Settings"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599618"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ee274e93-1ea2-4eda-a38b-f5484f7a2ddb"
	ownershipId="IntuneCxP_Intune"
/>

# Configure Devices - Configure Wifi Settings

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**I'm deploying a Wi-Fi profile that is dependent on a deployed certificate specified in the Wi-Fi profile. However, the configuration profiles are showing an error status.**
Check that your device received the certificate.

1.	In Intune, go to **All Devices** and select the device > **Device configuration**. 
2.	Check that all expected profiles are listed and in a successful state.

If you have intermediate certificates in your certificate chain, make sure those are deployed to Android devices. To check the certificate status, go to **Device configuration > Profiles > Android intermediate CA > Properties > Trusted Certificate**.

If you continue to see errors, review the procedures and troubleshooting sections in the Intune [SCEP](https://docs.microsoft.com/intune/certificates-scep-configure) or [PKCS](https://docs.microsoft.com/intune/certficates-pfx-configure) documentation.

**I deployed a Wi-Fi profile to a device. Intune is showing that it was successful, but the device is not connecting to Wi-Fi.**
A successful status means that Intune has successfully deployed the profile as configured. However, these settings may not match your network and/or authentication requirements. Review the logs in the infrastructure and authentication service for more details about the attempted deployment. You may need to work with your network infrastructure team, or the third-party equipment vendor, to gather and review logs.

## **Recommended documents**

* [How to configure Wi-Fi settings in Microsoft Intune](https://docs.microsoft.com/intune/wi-fi-settings-configure)<br>
* [Troubleshooting device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-troubleshoot)<br>
* [Wi-Fi settings for Android and Android for Work devices in Microsoft Intune](https://docs.microsoft.com/intune/wi-fi-settings-android)<br>
* [Wi-Fi settings for iOS devices in Microsoft Intune](https://docs.microsoft.com/intune/wi-fi-settings-ios)<br>
* [Wi-Fi settings for macOS devices in Microsoft Intune](https://docs.microsoft.com/intune/wi-fi-settings-macos)<br>
* [How to import Wi-Fi settings for Windows 8.1 and later devices in Microsoft Intune](https://docs.microsoft.com/intune/wi-fi-settings-import-windows-8-1)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
