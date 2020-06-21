<properties
	pageTitle="Enrolling a Windows 10 PC via MDM fails with error code 0x801c0003"
	description="Enrolling a Windows 10 PC via MDM fails with error code 0x801c0003"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="device_enrollment_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a48fb80c-f74e-4b62-b463-568a06320322"
	ownershipId="IntuneCxP_Intune"
/>

# Enrolling a Windows 10 PC via mobile device management fails with a "0x801c0003" error code.

## **Recommended steps**

You may encounter this problem if:

* The device cap is reached.  To enroll a new device, retire an existing one and try again.
* **Allow Devices to join Azure AD** is set to **None**.  To modify this setting open the Intune Azure portal > **Azure Active Directory** > **Devices** > **Device Settings** and change the value to **All** or **Selected**.
* The device has already been enrolled by another user. Go to **Devices** to verify that it does not already exist as an enrolled device.  
* The device is Windows 10 Home.  Azure Active Directory only supports the Windows 10 Pro, Education, and Enterprise editions. 



