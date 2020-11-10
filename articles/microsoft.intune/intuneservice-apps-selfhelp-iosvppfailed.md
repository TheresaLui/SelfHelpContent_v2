<properties
	pageTitle="I assigned an iOS VPP app to my users, but the installation failed."
	description="I assigned an iOS VPP app to my users, but the installation failed."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="apps_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d35d2d56-e591-489a-8f6a-9c28da0ae6e4"
	ownershipId="IntuneCxP_Intune"
/>

# I assigned an iOS VPP app to my users, but the installation failed.

## **Recommended steps**

Installation failures will occur in either of the following scenarios.

* A single VPP token is used across multiple mobile device management providers. VPP tokens from Apple may only be used with one provider. If you used a VPP token with multiple providers, you must re-upload the token to Intune. For more information about VPP apps [see the Intune documentation.](https://docs.microsoft.com/intune/vpp-apps-ios#before-you-start)  

* The total number of installations exceed the number of licenses. To view a usage report for your licenses, go to the Intune **Mobile apps > App licenses** page.  To learn how to reclaim licenses in use, see the Intune documentation about [Revoking app licenses and deleting tokens.](https://docs.microsoft.com/intune/vpp-apps-ios#revoking-app-licenses-and-deleting-tokens)
