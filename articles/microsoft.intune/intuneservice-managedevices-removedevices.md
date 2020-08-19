<properties
	pageTitle="Manage Devices - Remove Devices"
	description="Manage Devices - Remove Devices"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599668"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a92a1869-ccb8-4951-9844-de3c36b2e52d"
	ownershipId="IntuneCxP_Intune"
/>

# Manage Devices - Remove Devices

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**I issued a remote action to remove company data from a device, and now it's stuck in a pending state.**

For a remote action to successfully complete, the targeted device must be online and healthy. In the following situations, the remote action will stay in a pending state for 30 days, or until the device acknowledges the command:
	
* When the device does not have connectivity
* When the device loses its management status with Intune

If you think a device is no longer checking in, and that it won't be able to remove company data, click Delete. Deleting removes the device record so that it no longer appears in the Intune list of devices. If the device becomes active again, its user will have to re-enroll it.

## **Recommended documents**

* [Remove devices by using factory reset or remove company data](https://docs.microsoft.com/intune/devices-wipe)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
