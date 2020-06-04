<properties
	pageTitle="My iOS users are able to save corporate data outside of policy protected apps by using the Open In extension"
	description="My iOS users are able to save corporate data outside of policy protected apps by using the Open In extension"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="apps_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d50bdc08-0270-4aea-9d5e-3588c1a7b52d"
	ownershipId="IntuneCxP_Intune"
/>

# My iOS users are able to save corporate data outside of policy protected apps by using the Open In extension.

## **Recommended steps**

This is expected behavior on a device running iOS 11.  When the Open In extension is used, the policy protected app encrypts the file first, and then transfers it to the non-managed app. When opened in the non-managed app, the copied data is protected and unreadable. To verify this behavior, try to open a file after you transfer it to a non-managed app. 

New files aren't considered "corporate data" until you save them to a corporate policy protected location, such as OneDrive for business.    

