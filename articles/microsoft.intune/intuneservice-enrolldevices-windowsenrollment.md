<properties
	pageTitle="Diagnose and resolve issues experienced when attempting to enroll devices via Windows Enrollment"
	description="Diagnose and resolve issues experienced when attempting to enroll devices via Windows Enrollment"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	ms.author="jlynn"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32599687"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="86945c81-28a8-43c9-b32a-9ba1bb4360e6"
	ownershipId="IntuneCxP_Intune"
/>

# Diagnose and resolve issues experienced when attempting to enroll devices via Windows Enrollment

## **Recommended Steps**

Below are several common Windows enrollment failure scenarios, and how to resolve them:

**Installation of the PC client software fails with "The software cannot be installed, 0x80cf4017"**

This error occurs when your account certificate has expired. Re-download the PC Client software package in the Intune Admin Console. For more information please review [this documentation](https://docs.microsoft.com/intune-classic/deploy-use/install-the-windows-pc-client-with-microsoft-intune).

**Enrolling a Windows 10 PC via MDM fails with error code "0x801c0003"**

The error can occur in the following scenarios:

* The user has too many devices enrolled. Modify how many devices a user can enroll [here](https://portal.azure.com/#blade/Microsoft_Intune_Enrollment/OverviewBlade/enrollmentRules). If at the max, [retire a device](https://docs.microsoft.com/intune/devices-wipe) so a new one can be enrolled.
* "Users may join devices to Azure AD" is set to "none". You can change this to all or select users. See Azure Active Directory documentation [here](https://docs.microsoft.com/azure/active-directory/device-management-azure-portal#configure-device-settings) for more info.  
* The device is already enrolled by another user. Confirm if the device is enrolled by another user and either retire from the Azure Intune console or manually unenroll the device before trying again.
* The device is Windows 10 Home. Only Windows 10 Pro, Education and Enterprise skus are allowed to join Azure Active Directory.  

**Enrolling Windows 10 PC via MDM fails with "0x80180014" and error message "There was a problem. Your organization does not support this version of Windows."**

This error occurs when [device restrictions](https://portal.azure.com/#blade/Microsoft_Intune_Enrollment/OverviewBlade/enrollmentRules) prevent the Windows 10 device from enrolling. For more information on device restrictions and how to configure please review [this documentation](https://docs.microsoft.com/intune/enrollment-restrictions-set).

**"User License Type Invalid" or "User Name Not Recognized" error message during enrollment**

The user is not assigned an Intune or EMS license. You can assign licenses to each of your users in the [Azure Portal](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/All users) or the [Office 365 Admin Center](https://portal.office.com/adminportal). For more information on how to license users, please review [Azure user licensing](https://docs.microsoft.com/azure/active-directory/license-users-groups) or [Office 365 user licensing](https://docs.microsoft.com/intune/licenses-assign).

If you're still blocked, review these resources to help resolve your issues:

* The [Intune Troubleshooting Portal](https://aka.ms/intunetroubleshooting1) allows you to easily look up detailed information on a user's enrollment issue.  It also provides resolutions for many common enrollment failures.
* The [Intune Windows Troubleshooting Guide](https://support.microsoft.com/help/4089533/troubleshooting-windows-device-enrollment-problems-in-microsoft-intune) has a list of common errors that prevent enrollment and resolutions to each
* Lastly, [this document](https://docs.microsoft.com/intune-classic/troubleshoot/troubleshoot-device-enrollment-in-intune) has a list of common errors that prevent enrollment and resolutions to each.

Below is a list of additional resources and documentation that may also assist in resolving your issue. Please review them before opening a support case.

## **Recommended Documents**

* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Enroll Windows devices](https://docs.microsoft.com/intune/windows-enroll)<br>
* [Turn on auto-MDM enrollment with Azure Active Directory (AD) and Microsoft Intune](https://blogs.technet.microsoft.com/enterprisemobility/2015/08/14/windows-10-azure-ad-and-microsoft-intune-automatic-mdm-enrollment-powered-by-the-cloud/)<br>
* [Mobile Device Enrollment scenarios not supported](https://aka.ms/buvm2o)<br>
* [Choose how to manage devices](https://docs.microsoft.com/intune/get-started/choose-how-to-manage-devices)<br>
* [Enrolling Windows PCs as mobile devices](https://aka.ms/tboly1)<br>
* [Manage Windows PCs with Intune PC client software](https://docs.microsoft.com/intune/deploy-use/manage-windows-pcs-with-microsoft-intune)<br>
* [Deploy Intune client software as part of an image](https://aka.ms/jwvqq1)<br>
* [Intune Deployment Planning, Design and Implementation Guide](https://docs.microsoft.com/intune-classic/plan-design/introduction?toc=/intune/toc.json&bc=/enterprise-mobility/toc.json)<br>
* [Azure AD Join vs Azure AD Device Registration](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-plan)<br>
* [Turn on auto-MDM enrollment with Azure Active Directory (AD) and Microsoft Intune](https://blogs.technet.microsoft.com/enterprisemobility/2015/08/14/windows-10-azure-ad-and-microsoft-intune-automatic-mdm-enrollment-powered-by-the-cloud)<br>
