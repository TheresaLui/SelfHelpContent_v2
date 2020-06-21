<properties
	pageTitle="I issued a remote action to remove company data from a device, and now it's stuck in a pending state."
	description="I issued a remote action to remove company data from a device, and now it's stuck in a pending state."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devices_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1133464b-5b3f-4f8f-a9e9-4900e891599b"
	ownershipId="IntuneCxP_Intune"
/>

# I issued a remote action to remove company data from a device, and now it's stuck in a pending state. 

## **Recommended steps**

For a remote action to successfully complete, the targeted device must be online and healthy. In the following situations, the remote action will stay in a pending state for 30 days, or until the device acknowledges the command:
	
* When the device does not have connectivity
* When the device loses its management status with Intune

If you think a device is no longer checking in, and that it won't be able to remove company data, click Delete. Deleting removes the device record so that it no longer appears in the Intune list of devices. If the device becomes active again, its user will have to re-enroll it.
