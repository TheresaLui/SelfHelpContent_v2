<properties
	pageTitle="Manage Apps - Work with volume purchased apps and books"
	description="Manage Apps - Work with volume purchased apps and books"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599688"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="42fa2f90-e411-4af9-a81c-b97abce6f922"
	ownershipId="IntuneCxP_Intune"
/>

# Manage Apps - Work with volume purchased apps and books

Let's take a look at a few common issues deploying VPP Apps and e-books and how to resolve them:

**VPP Apps**

**I assigned an iOS VPP app to my users, but the installation failed.**

Installation failures will occur in either of the following scenarios.

* A single VPP token is used across multiple mobile device management providers. VPP tokens from Apple may only be used with one provider. If you used a VPP token with multiple providers, you must re-upload the token to Intune. For more information about VPP apps [see the Intune documentation.](https://docs.microsoft.com/intune/vpp-apps-ios#before-you-start)  

* The total number of installations exceed the number of licenses. To view a usage report for your licenses, go to the Intune **Mobile apps > App licenses** page.  To learn how to reclaim licenses in use, see the Intune documentation about [Revoking app licenses and deleting tokens.](https://docs.microsoft.com/intune/vpp-apps-ios#revoking-app-licenses-and-deleting-tokens)

**Users receive various prompts when they attempt to install VPP apps.**

Users receive varied VPP prompts based on:

* Device enrollment type.
* How the app is deployed.
* If the device or user group is targeted.

For a list of why your users are receiving VPP prompts, refer to the [End-User Prompts for VPP](https://docs.microsoft.com/intune/vpp-apps-ios#end-user-prompts-for-vpp) table in the Intune documentation.

**E-books**

**A user in my organization doesn't have the Apple iBooks app to view e-books.  Can I use Intune to install it?**

The iBooks app must be manually installed by the user from the Apple App Store. Intune is not able to install built-in Apple apps.

**I want to distribute my organization's in-house e-books to iOS devices.**

At this time, Intune does not support the distribution of in-house e-books.

**I assigned an e-book to a user's device, but now I want to unassign it.**

You cannot reclaim a license once the book has been assigned.

**Users are prompted to join the Apple VPP when they try to install e-books. How can I prevent these prompts?**

To prevent sign-up prompts, assign e-book licenses to security groups that have managed Apple IDs. The Apple ID assigned to the security group must match the Apple ID used on the device.

**My e-book is not showing up in the Intune portal.**

Intune syncs with the Apple Volume Purchase Program (VPP) services twice a day.  You can initiate a manual Apple VPP sync anytime.  To learn how to manage iOS apps purchased through Apple VPP, see the [Intune documentation.](https://docs.microsoft.com/intune/vpp-apps-ios#to-get-and-upload-an-apple-vpp-token)

Below is a list of additional resources and documentation that may also assist in resolving your issue.  Please review before opening a support case.

## **Recommended documents**

[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
[Manage volume-purchased apps and books with Intune](https://docs.microsoft.com/intune/vpp-apps)<br>
[What is Intune app management?](https://docs.microsoft.com/intune/app-management)<br>
[How to manage iOS apps purchased through a volume-purchase program with Intune](https://docs.microsoft.com/intune/vpp-apps-ios)<br>
[How to manage apps you purchased from the Microsoft Store for Business with Intune](https://docs.microsoft.com/intune/windows-store-for-business)<br>
[How to manage iOS eBooks you purchased through a volume-purchase program with Intune](https://docs.microsoft.com/intune/vpp-ebooks-ios)<br>