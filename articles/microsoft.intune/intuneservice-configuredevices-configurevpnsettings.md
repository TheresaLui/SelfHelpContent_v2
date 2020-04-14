<properties
	pageTitle="Configure Devices - Configure VPN Settings"
	description="Configure Devices - Configure VPN Settings"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599617"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1a9ffda7-13b1-4e9f-9083-ebd9bf9aafd0"
	ownershipId="IntuneCxP_Intune"
/>

# Configure Devices - Configure VPN Settings

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**When I configure a custom VPN for iOS, the per-app VPN feature isn't made available.**

Per-App VPN for iOS devices in Intune is currently only available to a specific [list of providers and partners](https://docs.microsoft.com/intune/vpn-setting-configure-per-app). You also must meet the certificate prerequisites before configuring a Per-App VPN. 

See the [Intune documentation](https://docs.microsoft.com/intune/vpn-settings-configure) for information about all VPN connection types in Intune.

**I deployed a VPN profile to a device. Intune is showing that it was successful, but the device is not connecting to the VPN.**

A successful status means that Intune has successfully deployed the profile as configured. However, these configurations may not match your network and/or authentication requirements. Review logs in the infrastructure and authentication service for more details about the attempted connection. You may need to work with your network infrastructure team, or the third-party VPN vendor, to gather and review logs.

## **Recommended documents**

* [How to configure VPN settings in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-configure)<br>
* [Troubleshooting device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-troubleshoot)<br>
* [Set up Per-App VPN in Microsoft Intune for iOS devices](https://docs.microsoft.com/intune/vpn-setting-configure-per-app)<br>
* [VPN settings for Android devices in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-android)<br>
* [VPN settings for iOS devices in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-ios)<br>
* [VPN settings for macOS devices in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-macos)<br>
* [VPN settings for Windows 10 devices in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-windows-10)<br>
* [VPN settings for Windows 8.1 devices in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-windows-8-1)<br>
* [VPN settings for Windows Phone 8.1 devices in Microsoft Intune](https://docs.microsoft.com/intune/vpn-settings-windows-phone-8-1)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
