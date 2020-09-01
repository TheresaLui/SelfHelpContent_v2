<properties
	pageTitle="Manage Apps - Use app protection policies"
	description="Manage Apps - Use app protection policies"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599681"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="823d4f82-3932-43ba-8498-6a42198edb34"
	ownershipId="IntuneCxP_Intune"
/>

# Manage Apps - Use app protection policies

## **Recommended Steps**

Let's review a few common issues deploying and using App Protection policies

**My user's applications are not adhering to the application protection policy settings I assigned them.**

See the Microsoft TechNet article [about Intune app protection diagnostics and managed browser bookmarks.](https://blogs.technet.microsoft.com/cbernier/2018/02/05/intune-app-protection-diagnostics-and-managed-browser-bookmarks/) This article describes how to use an Intune-managed browser to troubleshoot app protection.  You can use this to check that an app's status matches what you deployed to the user.

If the policy shown in the managed browser does not match what you deployed to the user, verify that you've met the following requirements:

* User has an Intune or EMS license.
* User belongs to a group that is targeted by the application protection policies.
* Only one corporate user is signed in to the device's protected apps.

Application protection policies only protect data accessed from a cloud service, such as Exchange Online and SharePoint Online from Office365. Data accessed from an on-premises source is not subject to the application protection policy. If you operate in a hybrid environment, this is important to check for each user, since access locations may vary.

If you target multiple app protection policies to a user, Intune applies only the most secure settings.  

New files aren't considered "corporate data" until you save them to a corporate policy- protected location, such as OneDrive for business.

**I enabled an app protection policy that does not require device enrollment. However, users are still being prompted to set a device PIN.**

When you enable Encrypt app data, your users may be required to set up and use a PIN to access their device. For more information about this setting's behavior, see the [Data relocation settings, Encrypt app data setting](https://docs.microsoft.com/intune/app-protection-policy-settings-ios#data-relocation-settings) in the Intune documentation.

**When I try to add a second account to an existing Outlook profile in the Outlook mobile app, I receive an error.**

Only one corporate user can be signed in to a device's protected apps. This includes devices that are signed in to the app already and the user if the device is enrolled.   

* For more information pertaining to iOS apps, see the Intune article, [What to expect when your iOS app is managed by app protection policies.](https://docs.microsoft.com/intune/app-protection-enabled-apps-ios)
* For more information pertaining to Android apps, see the Intune article, [What to expect when your Android app is managed by app protection policies.](https://docs.microsoft.com/intune/app-protection-enabled-apps-android)

**My iOS users are able to save corporate data outside of policy protected apps by using the Open In extension.**

This is expected behavior on a device running iOS 11.  When the Open In extension is used, the policy protected app encrypts the file first, and then transfers it to the non-managed app. When opened in the non-managed app, the copied data is protected and unreadable.     To verify this behavior, try to open a file after you transfer it to a non-managed app. 

New files aren't considered "corporate data" until you save them to a corporate policy- protected location, such as OneDrive for business.

## **Recommended documents**

[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
[What are app protection policies?](https://docs.microsoft.com/intune/app-protection-policy)<br>
[What is Microsoft Intune app management?](https://docs.microsoft.com/intune/app-management)<br>
[How to create and assign app protection policies](https://docs.microsoft.com/intune/app-protection-policies)<br>
[How to validate your app protection policy setup](https://docs.microsoft.com/intune/app-protection-policies-validate)<br>
[Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)<br>
[Intune-enlightened apps](https://www.microsoft.com/cloud-platform/microsoft-intune-apps)<br>






