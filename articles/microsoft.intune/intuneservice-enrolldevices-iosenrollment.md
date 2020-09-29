<properties
	pageTitle="Enroll Devices - iOS Enrollment"
	description="Enroll Devices - iOS Enrollment"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32599644"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ec7cea88-2266-4345-b838-e3ab24c00890"
	ownershipId="IntuneCxP_Intune"
/>

# Enroll Devices - iOS Enrollment

## **Recommended steps**

Start troubleshooting enrollment issues with the [Intune Troubleshooting Portal.](data-blade:Microsoft_Intune_DeviceSettings.TroubleshootBlade)<br>

The Troubleshooting Portal helps you easily look up detailed information on a user's enrollment issue.  It also provides resolutions for many common enrollment failures.  Review the Troubleshooting Portal documentation [here](https://docs.microsoft.com/intune/help-desk-operators).

Let's take a look at a few common iOS enrollment error messages and how to resolve them:

**"Device Cap Reached"** - This issue occurs if the user tries to enroll more devices than the device enrollment limit.  You can modify how many devices a user can enroll [here](https://portal.azure.com/#blade/Microsoft_Intune_Enrollment/OverviewBlade/enrollmentRules).  If at the max, [retire a device](https://docs.microsoft.com/intune/devices-wipe) so a new one can be enrolled.

**DEP device unable to enroll if MFA enabled** - Currently MFA(Multi-Factor Authentication) is not supported for DEP enrollment.  Please disable MFA to allow users to enroll devices.

**"This Service is not supported.  No Enrollment Policy"** - Apple Push Notification Service (APNS) has not been configured or has expired.  Review [this document](https://docs.microsoft.com/intune/apple-mdm-push-certificate-get#steps-to-get-your-certificate) for details on how to set up or renew your Intune account for Apple enrollment.

**"User License Type Invalid" or "User Name Not Recognized" error message during enrollment** - The user is not assigned an Intune or EMS license.  You can assign licenses to each of your users in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal).  For more information on how to license users please review [Azure user licensing](https://docs.microsoft.com/azure/active-directory/license-users-groups) or [Office 365 user licensing](https://docs.microsoft.com/intune/licenses-assign).

If you're still blocked review these resources to help resolve your issues:

The [Intune iOS Troubleshooting Guide](https://support.microsoft.com/help/4039809/troubleshooting-ios-device-enrollment-in-intune) has a list of common errors that prevent enrollment and resolutions to each.

Lasty, [this document](https://docs.microsoft.com/intune-classic/troubleshoot/troubleshoot-device-enrollment-in-intune) has a list of common errors that prevent enrollment and resolutions to each.

Below is a list of additional resources and documentation that may also assist in resolving your issue.  Please review before opening a support case.

## **Recommended documents**

[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
[Learn how to Enroll iOS devices in Intune](https://docs.microsoft.com/intune/ios-enroll)<br>
[Learn how to Enroll corporate-owned Device Enrollment Program iOS devices](https://docs.microsoft.com/intune/deploy-use/ios-device-enrollment-program-in-microsoft-intune#steps-to-enroll-ios-devices-by-using-apple-dep-management)<br>





