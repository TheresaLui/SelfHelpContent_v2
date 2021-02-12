<properties
	pageTitle="Enroll Devices - Android enrollment"
	description="Enroll Devices - Android enrollment"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="3"
	selfHelpType="generic"
	supportTopicIds="32599597"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="65656556-e586-4025-b0c0-dbb2af65c481"
	ownershipId="IntuneCxP_Intune"
/>

# Enroll Devices - Android enrollment

## **Recommended steps**

Let's take a look at a few common Android enrollment issues and how to resolve them:

**Device cannot complete enrollment because of "Device not Encrypted" error message in Company Portal** - Newer versions of Android, particularly starting with v7.0, require a startup passcode to make sure that your device is fully encrypted. Different device manufacturers have varying descriptions and locations for the startup passcode. Most of the time, this setting is referred to as "Secure Startup."  Common solutions are to enable a startup pin or fully encrypt the device.  For more information review [this document](https://docs.microsoft.com/intune-user-help/your-device-appears-encrypted-but-cp-says-otherwise-android).

**Devices fail to check in with the Intune service or display as "Unhealthy" in the Intune admin console** - Some Samsung 4.4 and 5.5 devices may not check into the service.  There are 3 possible solutions to this issue:  **1.** Manually open the Intune Company Portal app, which will automatically initiate a device sync. **2.** Update the device to Android 6.0 or higher **3.** Disable Samsung Smart Manager from managing the Intune Company Portal.  Review [this document](https://docs.microsoft.com/intune-classic/troubleshoot/troubleshoot-device-enrollment-in-intune#devices-fail-to-check-in-with-the-intune-service-and-display-as-unhealthy-in-the-intune-admin-console) for further details on these issues and resolutions.

**"User License Type Invalid" or "User Name Not Recognized" error message during enrollment** - The user is not assigned an Intune or EMS license.  You can assign licenses to each of your users in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal).  For more information on how to license users please review [Azure user licensing](https://docs.microsoft.com/azure/active-directory/license-users-groups) or [Office 365 user licensing](https://docs.microsoft.com/intune/licenses-assign).

If you're still blocked review these resources to help resolve your issues:

[Intune Troubleshooting Portal](https://aka.ms/intunetroubleshooting1) allows you to easily look up detailed information on a user's enrollment issue.  It also provides resolutions for many common enrollment failures.  Review the Troubleshooting Portal documentation [here](https://docs.microsoft.com/intune/help-desk-operators).

Lasty, [this document](https://docs.microsoft.com/intune-classic/troubleshoot/troubleshoot-device-enrollment-in-intune) has a list of common errors that prevent enrollment and resolutions to each.

Below is a list of resources and documentation that may also assist in resolving your issue.  Please review before opening a support case.

## **Recommended documents**

[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Learn how to Enroll Android devices](https://docs.microsoft.com/intune/android-enroll)<br>


