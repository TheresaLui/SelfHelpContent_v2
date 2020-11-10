<properties
	pageTitle="My user's applications are not adhering to the application protection policy settings I assigned them."
	description="My user's applications are not adhering to the application protection policy settings I assigned them."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="apps_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="73fe5bde-f948-409f-8723-7e994fa4613c"
	ownershipId="IntuneCxP_Intune"
/>

# My user's applications are not adhering to the application protection policy settings I assigned them.

## **Recommended steps**

See the Microsoft TechNet article [about Intune app protection diagnostics and managed browser bookmarks.](https://blogs.technet.microsoft.com/cbernier/2018/02/05/intune-app-protection-diagnostics-and-managed-browser-bookmarks/) This article describes how to use an Intune-managed browser to troubleshoot app protection.  You can use this to check that an app's status matches what you deployed to the user.

If the policy shown in the managed browser does not match what you deployed to the user, verify that you've met the following requirements:

* User has an Intune or EMS license.
* User belongs to a group that is targeted by the application protection policies.
* Only one corporate user is signed in to the device's protected apps.

Application protection policies only protect data accessed from a cloud service, such as Exchange Online and SharePoint Online from Office365. Data accessed from an on-premises source is not subject to the application protection policy. If you operate in a hybrid environment, this is important to check for each user, since access locations may vary.

If you target multiple app protection policies to a user, Intune applies only the most secure settings.  

New files aren't considered "corporate data" until you save them to a corporate policy protected location, such as OneDrive for business.
