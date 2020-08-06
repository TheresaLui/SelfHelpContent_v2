<properties
	pageTitle="Configure Devices - Configure device restrictions"
	description="Configure Devices - Configure device restrictions"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599609"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="82c90ca0-5633-4655-b506-98eddfece94a"
	ownershipId="IntuneCxP_Intune"
/>

# Configure Devices - Configure device restrictions

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**I'm deploying a Windows 10 policy and it's not applying to the device.**
 
* Check to make sure that the policy is compatible with the Windows 10 build (such as 1709 and 1803) and version (such as Pro and Enterprise) that's on the device. For more information about specific policies and their supported Windows 10 products, see the [configuration service provider reference](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference).
* Go to [Troubleshoot](https://portal.azure.com/#blade/Microsoft_Intune_DeviceSettings/ExtensionLandingBlade/troubleshooting) to make sure the configuration profile is correctly assigned.
* Go to **Device configuration** to view the status of the deployment, and check for failures and errors. To learn how to collect logs and diagnose errors, view the [Intune documentation](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10).   

**I'm deploying an iOS or Android policy and it's not applying to the device.**

* Check that the policy is compatible with the OS version and device type. For example, policies for iOS Supervised devices will not work on non-Supervised devices. Likewise, policies intended for Android 8.0+ will not work for older devices.  
* Make sure the policy is correctly targeted to the user or device.
* Use the Troubleshoot blade to look for errors and other problems. More information on using the Troubleshooting blade for policy issues can be found [here](https://aka.ms/policy_troubleshooting).

## **Recommended documents**

* [How to configure device restriction settings in Microsoft Intune](https://docs.microsoft.com/intune/device-restrictions-configure)<br>
* [Troubleshooting device profiles in Microsoft Intune](https://docs.microsoft.com/intune/device-profile-troubleshoot)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
