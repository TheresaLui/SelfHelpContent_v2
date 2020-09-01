<properties
	pageTitle="Manage Apps - Assign Apps"
	description="Manage Apps - Assign Apps"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599600"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f6ca8359-0a1e-4a92-ae61-560062e07596"
	ownershipId="IntuneCxP_Intune"
/>

# Manage Apps - Assign Apps

## **Recommended Steps**

Let's review a couple common mobile application installation/deployment issues.

**I've made updates to apps but I'm not seeing them in the Company portal app or on the device.**

* Make sure the device is enrolled and the targeted user is signed in to the Company Portal. 
* Make sure the user or device belongs to a group to which the application is assigned.
* Verify that you've assigned an Intune or EMS license to the targeted user.
* Confirm that the deployment type is listed as "available" or "required".

**I've made updates to apps but I'm not seeing them in the Company portal app or on the device.**

Sometimes apps fail to install because of device-side conditions. This can occur even when the deployment and installation commands work correctly. To ensure the device is in a state to install an app, verify that the device is:

* Turned on.
* Charged.
* Connected to the internet.
* Set up with an Apple ID, Google Play account, or Microsoft Account, if applicable.

Also make sure that the app version you are installing is newer than the version that is currently on your devices. 

See the Intune documentation [for more information about adding line-of-business apps.](https://docs.microsoft.com/intune/apps-add#next-steps) In the article, go to Next steps and click the LOB apps page specific to your device platform.  

**I deployed an app to my users. I am now seeing an app installation error in Intune on the Mobile apps > App install status page.**

Review the [Intune documentation about system and browser requirements](https://docs.microsoft.com/intune/supported-devices-browsers) and make sure that the device meets:

* The app's requirements.
* Any admin-configured pre-requirements. 

For a list of common errors and solutions see the [Intune support blog post.](https://blogs.technet.microsoft.com/intunesupport/2018/05/15/error-codes-for-troubleshooting-app-installation-issues/)

**I assigned an iOS VPP app to my users, but the installation failed.**

Installation failures will occur in either of the following scenarios.

* A single VPP token is used across multiple mobile device management providers. VPP tokens from Apple may only be used with one provider. If you used a VPP token with multiple providers, you must re-upload the token to Intune. For more information about VPP apps [see the Intune documentation.](https://docs.microsoft.com/intune/vpp-apps-ios#before-you-start)  

* The total number of installations exceed the number of licenses. To view a usage report for your licenses, go to the Intune **Mobile apps > App licenses** page.  To learn how to reclaim licenses in use, see the Intune documentation about [Revoking app licenses and deleting tokens.](https://docs.microsoft.com/intune/vpp-apps-ios#revoking-app-licenses-and-deleting-tokens)

## **Recommended documents**

[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
[How to assign apps to groups with Microsoft Intune](https://docs.microsoft.com/intune/apps-deploy)<br>
[What is Microsoft Intune app management?](https://docs.microsoft.com/intune/app-management)<br>








