<properties
	pageTitle="A user received a new iOS device and restored it with data from an iCloud backup. The user is now able to access corporate email, even though the device has never been enrolled in Intune."
	description="A user received a new iOS device and restored it with data from an iCloud backup. The user is now able to access corporate email, even though the device has never been enrolled in Intune."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="conditional_access_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="36af45c6-665a-4efe-bb25-c6bb384ddc15"
	ownershipId="IntuneCxP_Intune"
/>

# A user received a new iOS device and restored it with data from an iCloud backup. The user is now able to access corporate email, even though the device has never been enrolled in Intune.

## **Recommended steps**

New iOS devices that are restored from an iCloud backup may also restore the access point name (APN).  If this occurs, Intune may recognize the new device as the user's previous device (or whichever device the backup came from) and mark it as compliant.
