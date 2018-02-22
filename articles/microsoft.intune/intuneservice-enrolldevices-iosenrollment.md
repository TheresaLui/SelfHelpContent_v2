<properties
	pageTitle="Enroll Devices - iOS Enrollment"
	description="Enroll Devices - iOS Enrollment"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32599644"
	resourceTags="intune_device_enrollment"
	productPesIds="15584"
	cloudEnvironments="public"
/>

# Enroll Devices - iOS Enrollment

## **Recommended steps**

Let's take a look at a couple common iOS enrollment error messages and how to resolve them:

**"This Service is not supported.  No Enrollment Policy"** - Apple Push Notification Service (APNS) has not been configured.  Review [this document](https://docs.microsoft.com/intune/apple-mdm-push-certificate-get#steps-to-get-your-certificate) for details on how to set up your Intune account for Apple enrollment.

**"User License Type Invalid or User Name Not Recognized"** - The user does not have the proper Intune or EMS license assigned to a user.  You can assign licenses to each of your users in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal/home#/homepage).  Review the user licensing documentation [here](https://docs.microsoft.com/intune/licenses-assign).

If you're still blocked review these resources to help resolve your issues:

[Intune Troubleshooting Portal](https://aka.ms/intunetroubleshooting1) allows you to easily look up detailed information on a user's enrollment issue.  It will also give resolutions for many common enrollment failures.  Review the Troubleshooting Portal documentation [here](https://docs.microsoft.com/intune/help-desk-operators).

The [Intune iOS Troubleshooting Guide](https://support.microsoft.com/help/4039809/troubleshooting-ios-device-enrollment-in-intune) has a list of common errors that prevent enrollment and resolutions to each.

Below is a list of resources and documentation that may assist in resolving your issue.  Please review before opening a support case.

## **Recommended documents**

[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
[Learn how to Enroll iOS devices in Intune](https://docs.microsoft.com/intune/ios-enroll)<br>
[Learn how to Enroll corporate-owned Device Enrollment Program iOS devices](https://docs.microsoft.com/intune/deploy-use/ios-device-enrollment-program-in-microsoft-intune#steps-to-enroll-ios-devices-by-using-apple-dep-management)<br>






